# Thread vs Runnable

|              | Thread                                     | Runnable                                                                                                                          |
| ------------ | ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| Typ          | Klasa abstrakcyjna                         | Interfejs                                                                                                                         |
| Kiedy używać | 1. Planujesz zastąpienie pozostałych metod | 1. Planujesz zastąpić jednie metodę `run`<br>2. Chcesz używać super klasy<br>3. Chcesz używać w wielu wątkach jednego obiektu<br> |
|              |                                            |                                                                                                                                   |

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
# `ThreadLocal<>`
`ThreadLocal` przydziela każdemu wątkowi osobny obiekt.
Posiada metody `set(...)`, `get()` i `remove()` 

> [!WARNING] UWAGA
> W `ThreadPool`u taski mogą używać tych samych wątków.
> ![[Pasted image 20240623125222.png]]

Można ustawić domyślną wartość początkową za pomocą `ThreadLocal.withInitial( () -> {return something;} )`
## InheritableThreadLocal<>
W przypadku gdy wątek tworzy wątek dziecko, ponieważ jest to inny wątek normalny `ThreadLocal` będzie traktował ten wątek jako osobny. W przypadku `InheritableThreadLocal` wątek dziecko odziedziczy wartość po rodzicu.
Posiada nadpisywalną metodę `T childValue(T parentValue)` która ustawia domyślną wartość dziecka. Można np. zinkrementować zmienną głębokość.
# Race Conditions
Występują wtedy kiedy operacja nie jest atomiczna, tzn że składa się z kilku elementów, np. czytanie, dodatnie 1, zapis.
W tym przypadku wątki mogą wykonać czytanie w tym samym momencie, i wtedy zapiszą tą samą wartość. Rozwiązaniem tego problemu jest `synchronized`, albo użycie atomicznej zmiennej. 
> [!WARNING] UWAGA
> W przypadku atomicznych zmiennych, atomiczne są jedynie metody. Użycie kilku atomicznych metod nie jest atomiczne.

# Współbieżność vs równoległe wykonywanie
Współbieżność polega na tym że jeden wątek wykonuje się przez pewną chwilę, a potem 2 wątek. 
Równoległość polega na tym że 2 wątki są wykonywane na raz na różnych CPU.

# Równoległość
To dzielenie jednego tasku na podtaski, które mogą być wykonywane równolegle.
# Interfejs Lock
Wątek może zablokować element typu `Lock` za pomocą metody `lock()`, kolejne wątki nie będą w stanie go zablokować i będą zmuszę no czekania.
Po zakończeniu krytycznej operacji należy wywołać metodę `unlock()` w celu odblokowania. `Lock` działa podobnie do `synchronized`
`import java.util.concurrent.locks.*`
W przypadku `ReentrantLock` pozwala on temu samemu wątki zablokować ten sam `Lock` kilka razy. W celu odblokowania należy go odblokować tyle samo razy co był zablokowany.
## Przykład
```java
public class CounterLock {
	private long count = 0;
	private Lock lock = new ReentreantLock();
	public void inc(){
		try {
			lock.lock();
			this.count++;
		}
		finally {
			lock.unlock();
		}
	}

}
```
## Sprawiedliwość
Podobnie jak `synchronized` `Lock` nie gwarantuje sprawiedliwości, tzn. że Kolejność w jakiej dany wątek otrzyma dostęp do `Lock` nie jest taka sama jak kolejność w której dany wątek doszedł do metody `lock`.
### Zapewnienie sprawiedliwości
W celu zapewnienia sprawiedliwości wystarczy dodać to konstruktora wartość `true`.
```java
private Lock lock = new ReentreantLock(true);
```
## Przerywanie oczekiwania na `Lock`
Ponieważ czas w którym wątek oczekuje na metodę `lock()` może być długi można posłużyć się metodą `lockInterruptibly()` która w przypadku w którym watek otrzyma przerwanie `interrupt()` wyrzuci `InterruptedException`
## `tryLock()`
Ta metoda w przeciwieństwie do metody `lock()` w przypadku w którym inny wątek blokuje, zwraca fałsz. Można zdefiniować timeout, czyli czas po którym metoda się poddaje, w tym przypadku należy również obsłużyć `InterruptedException`
### Przykład
```java
Lock lock = new ReentrantLock(true);
try {
	boolean lockStatus = lock.tryLock(3, TimeUnit.SECONDS);
}
catch(InterruptedException ex) {
	ex.printStackTrace();
}
if(lockStatus) {
	try {
		// do stuff
	}
	finally {
		lock.unlock();
	}
}
else {
	System.out.println("Failed to lock the lock");
}
```
## Metody `ReentrantLock`

| metoda                            | opis                                 |
| --------------------------------- | ------------------------------------ |
| `int getHoldCount()`              | Ile razy został zablokowany          |
| `int queueLength()`               | Ile wątków oczekuje na zamek.        |
| `boolean hasQueuedThread(Thread)` | czy dany wątek oczekuje w kolejce.   |
| `boolean hasQueuedThreads()`      | czy jakieś wątki oczekują w kolejce. |
| `boolean isFair()`                | czy jest sprawiedliwy.               |
| `boolean isLocked()`              | czy jest zablkowowany.               |
| `boolean isHeldByCurrentThread()` | czy aktualny wątek go wykonywuje.    |
## `Lock` vs `synchronized`

| właściwość                                              | `Lock` | `synchronized` |
| ------------------------------------------------------- | ------ | -------------- |
| Musi zawierać się w jednej metodzie?                    | NIE    | TAK            |
| Musi być Reentrant?                                     | NIE    | TAK            |
| Może gwarantować sprawiedliwość?                        | TAK    | NIE            |
| Można ustawić timeout?                                  | TAK    | NIE            |
| Czy można `interrupt` podczas oczekiwania na dostęp?    | TAK    | NIE            |
| Wymaga używania `try`/`finally` podczas odblokowywania? | TAK    | NIE            |
## DeadLock
To jest problem który wstępuję w którym 1 wątek blokuje zamek 1, a 2 wątek 2.
Następnie 1 wątek i 2 wątek próbują zablokować odpowiednio zamek 2 i 1. W tym przypadku oba wątki będą czekały w nieskończoność aż jeden z nich odblokuje zame.
![[Pasted image 20240623162625.png]]
# `ExecutorService`
Pozwala na stworzenie kolejki `Runnable` które będą rozpoczynane po kolei przez przypisane wątki.
## importy
```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
```
## Tworzenie
```java
ExecutorService executor = Executors.newFixedThreadPool(10);
```
Coś takiego stworzy $10$ wątków w których odbywać się będą `Runnable` taski.
## Dodanie nowego taska
### `execute()`
```java
for(int i = 0; i < 100; i++) {
	executor.execute(new Runnable() {
		@Override
		public void run(){
			String threadName = Thread.currentThread().getName();
			for(int i2 = 0; i2 < 100; i2++) System.out.println(threadName + " 🗣️ " + i2);
		}
	});
}
```
### `submit()`
Metoda ta działa podobnie, tylko zwraca obiekt typu `Future` na którym można:
### Future
#### Metoda `isDone()`
metoda `isDone()`
zwraca prawdę gdy `Runnable`/`Callable` zakończył działanie
#### metoda `get()`
czeka aż `Runnable`/`Callable` zakończy działanie, i zwraca zwróconą wartość. Należy obsłużyć `InterruptedException` oraz `ExecutionException`
#### Metoda `cancel(mayInterrupt)`
W przypadku w którym wykonywanie się jeszcze nie zaczęło, nie zacznie się ono nigdy.
W przeciwnym przypadku jeśli jest `mayInterrupt = true` to przerwie działanie taska.
W przypadku w którym nie uda się anulować, już wcześniej był anulowany lub ukończony, metoda zwróci `false`. 
Po wywołaniu `isDone()` będzie zawsze zwracało prawdę. Jeżeli metoda `cancel` zwróciła prawdę to metoda `isCancelled()` również zwróci parwdę. 


## Metoda `invokeAny((Collection) callables)`
Bierze i wykonuje wszystkie Callable i zwraca wynik pierwszego który zakończył. Należy obsłużyć wyjątki.
Zwraca wartość zwracaną przez obiekty Kolekcji.

## Metoda `invokeAll((Collection) callables)`
Zwraca kolekcje wszystkich wyników.
Wartość zwrócona to `List<Future<...>>`
## Zakończenie

Metoda `shutdown` blokuje możliwość dodawania nowych tasków do kolejki.
Alternatywnie można użyć metody `shutdownNow()` która blokuje dodawanie nowych tasków i wysyła wszystkim aktualnym przerwania.
Obie metody nie gwarantują zakończenia procesu.

```java
executor.shutdown();
```
W tym przypadku stworzy i zakolejkuje $100$ `Runnable`,  najpierw przez $10$ wątków zostanie wykonane $10$ `Runnable`, po tym zostanie wykonane kolejne $10$ `Runnable`, i tak dalej aż dojdzie do końca. Metoda `shutdown` zakańcza serwis po ukończeniu wszystkich tasków.
> [!WARNING] UWAGA
> Metoda nie jest blokująca, aby czekać na zakończnie należy użyć `awaitTermination`

### Oczekiwanie na zakończenie
```java
boolean awaitTermination(timeout, TimeUnit)
```
metoda czeka na zakończenie, przyjmuje czas oczekiwania oraz jednostkę czasu.
W przypadku w którym metoda nie doczeka się zamknięcia zwraca `false` w przeciwnym wypadku `true`.
Należy obsłużyć wyjątek `InterruptedException`.
# Klasy/interfejsy
## `BlockingQueue`
Interfejs który jeżeli kolejka jest pusta, blokuje operacje zabierania.
Jeżeli kolejka jest pełna to również blokuje dodawanie elementu.
Używana jest typowo dla przypadku w którym jeden wątek produkuje a 2 konsumuje.

Metody działające na pojedynczych elementach są wszystkie wątkowo bezpieczne. Metody grupowe nie są.

### Implementacje
#### `ArrayBlockingQueue`
Elementy przechowywane są w tablicy.
W konstruktorze podawany jest rozmiar.
#### `LinkedBlockingQueue`
Elementy są przechowywane w liście.
#### `LinkedBlockingDequeue`
 
#### `PriorityBlockingQueue`

### Metody

|             | **Throws Exception** | **Special Value** | **Blocks** | **Times Out**                 |
| ----------- | -------------------- | ----------------- | ---------- | ----------------------------- |
| **Insert**  | `add(o)`             | `offer(o)`        | `put(o)`   | `offer(o, timeout, timeunit)` |
| **Remove**  | `remove(o)`          | `poll()`          | `take()`   | `poll(timeout, timeunit)`     |
| **Examine** | `element()`          | `peek()`          |            |                               |

#### `drainTo(Collection, (opcjonalnie) maxElementow)`
Metoda pobiera elementy z kolejki do kolekcji.
# Typy Atomiczne
https://www.baeldung.com/java-atomic-variables
Obiekty atomiczne posiadają metody atomiczne, których nie można przepołowić i są przystosowane do działania w wielu wątkach.
# False Sharing
Procesor cachuje zmienne współdzielone przez wątki, w postaci bloków które często są większe niż same zmienne. W przypadku zmiany wartości współdzielonych przez 2 wątki, zmienne obok mogą również zostać oznaczone jako zmienione, mimo że się tak nie stało, to wymusi odświeżenie nawet nie zmienionych zmiennych, to jest **False Sharing**. False Sharing może znacznie obniżyć wydajność.

## Unikanie
Można rozdzielić zmienne za pomocą specjalnej adnotacji.
```java
@jdk.internal.jvm.annotation.Contended
```
Spowoduje to że zmienna zaanotwana tym będzie jedyną w bloku.
Ewentualnie można podzielić na grupy
```java
@jdk.internal.jvm.annotation.Contended("nazwa")
```
Można również w ten sposób oznaczyć klasę. Wtedy wszystkie pola będą rozdzielone.

```java
@jdk.internal.jvm.annotation.Contended
class Klasa {

}
```


> [!WARNING] Ostrzeżenie
> Czasami to oznaczenie może pogorszyć wydajność

# Thread Congestion
Występuje wtedy, kiedy kilka wątków próbuje uzyskać dostęp do np. metody zsynchronizowanej. W tym przypadku czas oczekiwania może być długi, i ogólnie to wątki marnują czas.
## Przeciwdziałanie
 W przypadku `BlockingQueue` można stworzyć kilka osobnych dla każdego wątku, i zrobić tak, aby producent rozdawał je po równo.

# Sygnałowanie wątków
Java posiada wbudowane mechanizmy pozwalające wątkom na stanie się nieaktywnymi do czasu do póki nie otrzymają sygnału.
## `wait()`
Ta metoda pozwala czekać na monitorze, dopóki nie wyśle on powiadomienia. Ta metoda musi być używana w bloku `synchronized` który ma ten sam monitor. Konieczne jest również obsłużenie wyjątku `InterruptedException`
### Przykład
```java
class stuff {
	Monitor monitor = new Monitor();

	public void doWait(){
		synchronized(monitor) {
			try {
				monitor.wait();
			}
			catch(InterruptedException) {
			}
		}
	}

}

```
## `notify()`
Wybudza ona tylko jeden wątek.
```java
class stuff {
	...

	public void doNotify() {
		synchronized(monitor) {
			monitor.notify();
		}
	}
}
```
W przypadku metody `notify` musi ona być wywołana w bloku `synchronized`




> [!WARNING] UWAGA
> W przypadku w którym wątek wyśle powiadomienie zanim 2 wątek zacznie czekać na sygnał, sygnał może zostać utracony, i wątek może czekać w nieskończoność. W celu zabezpieczania się przed tym warto mieć zmienną typu `boolean` która będzie ustawiana przed sygnałem, i sprawdzana przed rozpoczęciem czekania.

> [!WARNING] UWAGA
> Wątek może obudzić się bez otrzymania sygnału.
## `notifyAll()`
wybudza ona wszystkie wątki, działa podobnie do [[#`notify()`]]

# Inne Klasy przystosowane do pracy wielowątkowej

https://medium.com/javarevisited/java-collections-and-their-thread-safe-versions-9f715c26cace