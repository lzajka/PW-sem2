**Interfejsy** oraz **klasy abstrakcyjne** umożliwiają tworzenie częściowo bądź w ogóle nie zaimplementowanych klas. 

Interfejsy zawierają same [[Obiekty i Typy prymitywne#Podstawowe pojęcia|deklaracje]] metod, a wszystkie pola muszą być `public static final`.

Klasy abstrakcyjne mogą zawierać niezaimplementowane metody `abstract`.

Każda klasa może mieć **tylko jedną** klasę abstrakcyjną lub klasę jako rodzica.

Ponieważ **Interfejsy** oraz **Klasy abstrakcyjne** niekoniecznie są całkowicie zaimplementowane nie można bezpośrednio stworzyć ich instancji, konieczne jest stworzenie normalnej klasy dziedziczącej po ich.




# Różnica
Różnica polega na tym, że klasa abstrakcyjna może być częściowo zaimplementowana, a interfejs nie. Klasa abstrakcyjna używa `abstract class`, interfejs `interface` a normalna klasa `class`.
# Dziedziczenie
Klasy mogę dziedziczyć metody i pola (zmienne) po innych klasach lub interfejsach. Dziedziczone elementy można nadpisać, nazywa się to [[Przeciążenie i Przesłonięcie#Przesłonięcia|Przesłanianiem]].
> [!WARNING] UWAGA
> Konstruktory nie są dziedziczone i nie można ich przesłonić. Aby w konstruktorze wykonać konstruktor klasy nadrzędnej należy na początku konstruktora użyć metody `super()`. Ta metoda może przyjmować takie same argumenty jak konstruktor klasy nadrzędnej.
# Polimorfizm
Umożliwia nam traktowanie konkretnego obiektu jako klasę wyżej w hierarchii. 

```java
Pet myPet = new Cat();

myPet.pet();
```

W tym przypadku `Cat` jest podklasą `Pet`. Metody które zostały przesłonięte przez klasę `Cat` będą nadal przesłonięte w obiekcie `myPet`. W obiekcie `myPet` będę miał jedynie dostęp do metod i pól zdeklarowanych w `Pet`.

## Późne wiązanie
Jak widać w powyższym przykładzie to, że zmienna ma określony typ nie oznacza tego, że wiadomo jak zadziała dana metoda. Późne wiązanie oznacza to, że w czasie kompilacji kompilator nie przypisuje konkretnej sygnaturze metody (`typ nazwa(typy argumentów)`) konkretnego działania. W tym przypadku `myPet.pet()` jest przykładem późnego wiązania.

Klasy dziedziczmy za pomocą `extends`, interfejsy za pomocą `implements`
## Wczesne wiązanie
Jest wtedy kiedy w czasie kompilacji kompilator przypisuje danej sygnaturze metody działanie. 
# Przykłady
## Klasa abstrakcyjna
```java
abstract class Shape {
	protected String name;
	public abstract Double calculateArea();
	public String getName() {
		return this.name;
	}
	public Shape(){
		System.out.println("Stworzono nowy kształt");
	}
}
```
Klasa abstrakcyjna implementuję metodę `getName()` zwracającą nazwę figury, Każda figura rozszerzająca tą klasę abstrakcyjną będzie musiała zaimplementować własną metodę `calculateArea()`
```java
class Square extends Shape {
	int x;
	int y;
	@Override
	public Double calculateArea(){
		return new Double(x * y);
	}
	public Square(int a, int b){
		super();
		this.name = "Square";
		this.x = a;
		this.y = b;
	}
}
```
Metoda `super()` wywołuje konstruktor rodzica (`extend`).
Otrzymany object `Square` można wykorzystywać jako `Shape`
```java
public class Main{
    public static void main(String[] args) {
    
        Square sq = new Square(1, 10); 
        Shape s = sq;
        
        System.out.println("area: " + s.calculateArea());
        System.out.println("Shape: " + s.getName());
    }
}
```
## Interfejs
```java
interface Talkable {
	public String getNextDialogue();
}
```

```java
interface Follower {
	public String joinPlayer();
}
```
## Klasa dziedzicząca
```java
class QuestGiver extends NPC implements Talkable, Follower {
	// Konieczna jest implementacja wszystkich pozostalych klas
	public QuestGiver(){
	    super(100);
	}
	@Override
	public String getNextDialogue(){
	    return new String("Another settelment needs your help.");
	}
	@Override
	public String joinPlayer(){
	    return new String("Lead the way!");
	}
	
	
}
```

```java
public class Main{
    public static void main(String[] args){
        QuestGiver qg = new QuestGiver();
        
        Follower fw = qg;
        Talkable t = qg;
        
        System.out.println(fw.joinPlayer());
        System.out.println(t.getNextDialogue());
    }
}
```
## Łączenie interfejsów
```java
interface One{
	public int one();
}

interface Two{
	public int two();
}

interface OneAndTwo extends One, Two {
}
```
# Ważne interfejsy
- [[Comparator<T>]]
- [[Comparable<T>]]
- [[Iterable<T>]]