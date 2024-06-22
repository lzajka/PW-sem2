**Interfejsy** oraz **klasy abstrakcyjne** umożliwiają tworzenie częściowo bądź w ogóle nie zaimplementowanych klas. 

Każda klasa może mieć **tylko jedną** klasę abstrakcyjną jako rodzica.

Ponieważ **Interfejsy** oraz **Klasy abstrakcyjne** nie są całkowicie zaimplementowane nie można bezpośrednio stworzyć ich instancji, konieczne jest najpierw zaimplementowanie ich.

# Różnica
Różnica polega na tym, że klasa abstrakcyjna może być częściowo zaimplementowana, a interfejs nie.

# Przykłady
## Klasa abstrakcyjna
```java
abstract class Shape {
	protected String name;
	public abstract Double calculateArea();
	public String getName() {
		return this.name;
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
Metoda `super()` wywołuje konstruktor rodzica (`extend`),  w tym przypadku wykorzystanie go nie jest konieczne.
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

```java
class NPC {
    int health;
    public void dealDamage(int damage){
        health -= damage;
    }
    
    public NPC(int health) {class QuestGiver extends NPC implements Talkable, Follower {
	// Konieczna jest implementacja wszystkich pozostalych klas
}
        this.health = health;
    }
    
}
```

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