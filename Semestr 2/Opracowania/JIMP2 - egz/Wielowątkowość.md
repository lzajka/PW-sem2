# Thread vs Runnable

|              | Thread                                     | Runnable                                                                                                                          |
| ------------ | ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| Typ          | Klasa abstrakcyjna                         | Interfejs                                                                                                                         |
| Kiedy używać | 1. Planujesz zastąpienie pozostałych metod | 1. Planujesz zastąpić jednie metodę `run`<br>2. Chcesz używać super klasy<br>3. Chcesz używać w wielu wątkach jednego obiektu<br> |
|              |                                            |                                                                                                                                   |

# race-conditions
W przypadku jeżeli do jednej zmiennej może mieć dostęp metoda w wielu różnych wątkach może dojść do **race-condition**. 
## Przykłady
- Wypłacasz pieniądze z banku w 2 wątkach, konieczne jest sprawdzenie czy masz wystarczająco dużo pieniędzy, 2 metody przechodzą to wymaganie równocześnie, i odejmują ci, może dojść do przejścia na liczbę ujemną bądź integer overflow
- Jedna wartość jest zmieniana w 2 wątkach, W tym przypadku może dojść do tego że operacja będzie wykonywana na nieaktualnej wartości (z pominięciem wątku 1)
## Przeciwdziałanie
- synchronized
- atomicasd


# Thread

## Implementacja wątku

```java
class Scream extends Thread {
	private static int count = 0;
	private int ID = 0;
	private int amount;
	
	public Scream(int amount){
		super();
		this.ID = count++;
		this.amount = amount;
	}
	
	@Override
	public void run(){
		try {
			for(int i = 0; i < this.amount; i++){
				System.out.println("A (" + ID + ")");
				sleep(100);
			}
		}
		catch(InterruptedException ex){
			System.out.println("💀 (" + ID + ")");
		}
	}
}
```


## Startowanie i kończenie wątku
Za pomocą metody `start()` następnie czekamy aż się zakończy za pomocą metody `join()`, w przypadku braku `join()` program nie zakończy do momentu zakończenia wątku bądź, wymuszenia wyjścia.
Nie dotyczy to **daemonów** które są nisko priorytetowe i kończą działanie kiedy wszystkie pozostałe œatki się kończą.
```java
public class Main{
	public static void main(String[] args) {
		Scream scr0 = new Scream(10);
		Scream src1 = new Scream(20);
		Scream scr2 = new Scream(10000);
		scr2.setDaemon(true);
		scr0.start();
		scr1.start();
		scr2.start();
		try {
			scr0.join();
		}
		catch(InterrupedException ex) {
			ex.printStackTrace();
		}
		
		System.out.println("I'm done");
	}
}
```
W tym przypadku metoda `main` czeka aż wątek `scr0` się zakończy. Następnie przed wyjście czeka aż `scr1` się również zakończy, ponieważ `scr2` jest demonem, `scr2` kończy działanie wcześniej.
# Runnable
```java
public class Laugh extends Sound implements Runnable {
	private int totalLaughCount = 0;
	private int ID = 0;
	private static int instanceCount = 0;
	
	Laugh(){
		ID = instanceCount++;
	}
	@Override
	public synchronized void run(){
		try {
			for(; this.totalLaughCount < 100; this.totalLaughCount++){
				System.out.println("🏃 (" + ID + ") " + this.totalLaughCount + "/" + 100);
				sleep(100);
			}
		}
		catch(InterruptedException ex){
			System.out.println("💀 (" + ID + ")");
		}
	}
}
```


```java
public class Main{
	public static void main(String[] args) {
		Thread laughArray = new Thread[3];
		laughArray[0] = new Thread(new Laugh());
		laughArray[1] = new Thread(new Laugh());
		laughArray[2] = new Thread(new Laugh());
	
		laughArray[2].setDaemon(true);
		laughArray[0].start();
		laughArray[1].start();
		laughArray[2].start();
		try {
			laughArray[0].join();
		}
		catch(InterruptedException ex) {
			ex.printStackTrace();
		}
		
		System.out.println("I'm done");
	}
}
```

W tym wypadku wszystkie wątki kończą się równocześnie.
``
# `volatile`
Używane w przypadku w którym wartość zmiennej może zostać zmieniona w innym wątku. Przeciwdziała cachowaniu wartości zmiennej, bez użycia możliwe jest że wątek będzie czytał starą wersję zmiennej.


# `synchronized`
Blok kodu/metoda który może być wykonywany jedynie przez jeden wątek na raz.
Monitor to w tym przypadku obiekt na którym synchronizacja jest wykonywana. W przypadku metod jest to zawsze `this`
Metody i bloki oznaczone jako `synchronized` które posiadają taki sam monitor nie mogą być wykonywane równocześnie. 
Jako monitory można używać innych zainicjowanych obiektów.

> [!WARNING] UWAGA
> Kolejność w której dany wątek dostanie dostęp do bloku/metody `synchronized` nie koniecznie jest taki, jak kolejność wywołania. Nie ma kolejki.
> Przypadek w którym dany wątek nie otrzyma dostępu nazywa się **głodzieniem**.


### Przykład 1 - Metoda
```java
public synchronized void doStuff(){
	// do stuff here
}
```
### Przykład 2 - Blok
```java
public void doStuffV2(){
	synchronized(this) {
		// do stuff here
	}
}
```

## W metodach statycznych
Ponieważ metody statycznie nie należą do **instancji** klasy, a do **obiektu** klasy. `synchronized` używa również obiektu klasy jako monitora.

W przypadku metod `synchronized` nie trzeba niczego zmieniać.

W przypadku boków `synchronized` należy użyć `NazwaKlasy.class` jako monitora.
> [!WARNING] UWAGA
> Metody statyczne oraz metody lokalne nie są synchronizowane na tym samym monitorze.
### Przykład
```java
public class Balls {
	public static synchronized void doBall(){
		// do stuff
	}
	public static void doBall2() {
		synchronized(Balls.class) {
			// do stuff
		}
	}

}
```
## Ponowne wejście
W przypadku w którym jedna metoda zsynchronizowana będzie wywoływała inną metodę zsynchronizowaną, nie będzie nieskończonego oczekiwania, ponieważ skoro wątek trzyma zamek na monitorze, może on wejść bez problemu do wszystkich innych zsynchronizowanych po tym monitorze metod.

## Widzialność danych
`synchronized` przy wejściu aktualizuje cache, przy wyjściu od razu zapisuje do głównej pamięci.
> [!WARNING] UWAGA
> Dane pobierane poza `synchronized` mogą być nadal przestarzałe.
# ThreadLocal

# Zmienne atomiczne