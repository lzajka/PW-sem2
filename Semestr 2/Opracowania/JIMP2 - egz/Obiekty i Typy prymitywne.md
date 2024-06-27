https://www.baeldung.com/java-primitives-vs-objects

W Javie możemy wykorzystywać typy prymitywne oraz obiekty.
# Podstawowe pojęcia
**Referencja** - wskazanie do miejsca w pamięci
**Deklaracja** - Poinformowanie o istnieniu danego obiektu/zmiennej określonego typu. 
**Inicjalizacja** - Przypisanie początkowej wartości.
**Definicja** - Deklaracja oraz Inicjalizacja danego obiektu/zmiennej.

# Typ prymitywny
Przechowywany jest jako konkretna wartość. 
## Deklaracja
```java
int a;
```
## Inicjalizacja
```java
a = 2;
```
## Definicja
```java
int b = 3;
```
 
## Metody
Typy prymitywne oraz zmienne typu prymitywnego **nie posiadają żadnych metod**. Można je natomiast wykorzystać jako argument w metodach innych klas.
### Przykład - Konwersja String do int
```java
public class StringToInt{
   public static void main(String[] args) {
      String odpowiedz = new String("21");
      
      try{
         int liczba = Integer.parseInt(odpowiedz);
         System.out.println(liczba);

      }
      catch(NumberFormatException ex) {
         // W przypadku w którym to nie jest liczba
         ex.printStackTrace();
      }
      
   }
}
```
### Konwersja obiektu Integer do int
```java
public class Integer2int{
   public static void main(String[] args) {
      Integer a = Integer.valueOf(21);
      
      // Można tak
      int b = a;

      // Albo tak
      int c = a.intValue();

      System.out.println(a);
      System.out.println(b);
      System.out.println(c);
   }
}
```

## Przypisanie wartości
# Obiekt
## Deklaracja
```java
public class Str {
   public static void main(String[] args) {
	   String str;
   }
}
```
## Inicjalizacja
W przypadku obiektów można powiedzieć, że zmiennej `str` przypisana zostaje referencja do nowo utworzonego obiektu.
Obiekt tworzony jest za pomocą operatora `new` oraz konstruktora klasy.
```java
...
str = new String();
...
```

> [!WARNING] UWAGA
> W przypadku klas  (`Boolean`, `Byte`, `Short`, `Char`, `Integer`, `Float`, `Double`)  będących wrapperami typów prymitywnych (`boolean`, `byte`, `short`, `char`, `int`, `float`, `double`) zalecane jest użycie metody statycznej `valueOf()` przyjmującej jako argument typ prymitywny wrappera. Ponieważ wykorzystujemy metodę, a nie konstruktor **nie używamy** `new`. Istnieją również inne klasy których obiekty tworzy się za pomocą metody, a nie konstruktora.
> ```java
> ...
> dbl = Double.valueOf(3.14);
> ...
> ```

## Definicja
Jest to połączenie Deklaracji oraz Iinicjalizacji.
```java
public class Str {
   public static void main(String[] args) {
      String str = new String();
      String abc = new String("abc"); 
   }
}
```


