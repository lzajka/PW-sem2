# Przeciążenia
Przeciążenia umożliwiają wykonanie innej metody w zależności od podanych argumentów. Zwracany typ musi być zawsze taki sam.
## Przykład
```java
public class SaySomething{
	public void saySomething(){
		System.out.println("Something");
	}

	public void saySomething(String text){
		System.out.println(text);
	}

	public void saySomething(int number) {
		System.out.println("The number is: " + number);
	}
	
	
}
```
# Przesłonięcia
Przesłonięcia umożliwiają zastąpienie bądź implementację metody klasy przodka lub interfejsu. Przed metodą używamy adnotacji `@Override`. Konstruktora nie można przesłonić.
## Podstawowe przesłonięcia klasy Object
Każda klasa dziedziczy z klasy Object. Domyślnie poniższe metody działają na podstawie adresu pamięci. W większości przypadków takie zastosowanie jest niepoprawne. Zaleca się więc odpowiednio przesłonić poniższe metody.
### hashCode
Funkcja typu int zwracająca hasz, przydatna do indeksowania elementów w między innymi mapach.
```java
@Override
public int hashCode(){
	return 0;
}
```
### equals
Funkcja boolowska porównująca elementy.
```java
@Override
public boolean equals(Object o)
```
1. Najpierw sprawdzamy czy elementy są takiego samego typu
	`if (!(o instanceof ObiektPorównywany)) return false;`
2. Następnie castujemy
   `ObiektPorównywany op = (ObiektPorównywany) o;`
3. Ostatnim krokiem jest porównanie wartości zmiennych. Ponieważ oba obiekty są instancjami tej samej klasy, jest możliwość porównywania zmiennych prywatnych bezpośrednio.
### toString
Funkcja konwertująca zmienną na postać tekstową. 
```
@Override
public String toString(){
...
}
```
