https://www.baeldung.com/java-static-instance-initializer-blocks
Mamy 2 typy bloków inicjujących: statyczne i niestatyczne.
statyczne są wykonywane przy wczytaniu klasy. Niestatyczne są wykonywane przed wykonaniem konstruktora.
Ogólnie to statyczne można używać jak np. wiemy że wszystkie klasy będą miały jedną wartość zawsze taką samą.

> [!WARNING] UWAGA
> Bloki inicjulizujące nie są dziedziczone. Można je wykonać w klasie dziedziczącej za pomocą `super`

# Przykład - niestatyczna
```java
class withInitBlock {
	static int objectAmount = 0;
	int objectNumber;
	{
		objectNumber = objectAmount;
		objectAmount++;
	}

}
```
Zmienna [[Statyczność|statyczna]] `objectAmount` przechowuję ilość stworzonych obiektów danego typu. Blok inicjulizujący przypisuje number obiektowi oraz zwiększa `objectAmount`.
# Przykład - Statyczna
```java
class withStaticInitBlock{
	String operatingSystem;
	static {
		operatingSystem = System.getProperty("os.name")
	}
}
```
Ponieważ system operacyjny nie zmieni się podczas uruchomienia, można przenieść inicjalizacje do bloku statycznego. Zmienna `operatingSystem` zostanie ustalona podczas wczytania klasy.