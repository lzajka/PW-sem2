https://www.geeksforgeeks.org/exceptions-in-java/
# Definicja
- Zdarzenie, które zakłóca normalne działanie programu.
- Wyjątkowy Warunek (ang. Exceptional Condition) - problem z którym nie możesz sobie poradzić w danym kontekście
## Przykłady
1. InterruptedException
2. Dzielenie przez 0. W tym przypadku jeżeli chodzi o samo działanie to nie podzielisz, ale np. w wyższym kontekście 0 może znaczyć coś innego, lub to że powinieneś przejść na inną metodę.
# Konieczność obsłużenia wyjątków
Mamy 2 główne rodzaje wyjątków: sprawdzone i niesprawdzone pierwsze muszą znajdować się w bloku `try` `catch` lub metoda je zawierające musi zawierać `throws`, 2 rodzaj wyjątków niekoniecznie.

Wyjątki niesprawdzone dziedziczą po `RuntimeException` lub `Error`. Wszystkie pozostałe wyjątki są sprawdzone.
## Przykład
```java
class RException1 extends RuntimeException {

}

// Nadal dziedziczy po RuntimeException
class RException2 extends RException1 {

}

class Exception1 extends Exception {

}


class ThrowsException {
	public void musiZlapac() {
		try {
			throw new Exception1();
		}
		catch(Exception1 ex) {
			ex.printStackTrace();
		}
	}
	// teraz ktos kto bedzie uzywal tej metody bedzie musial ten wyjatek obsluzyc
	public void terazKtosInny() throws Exception2 {
		throw new Exception1();
	}
	// A tego nikt nie musi obsluzyc
	public void niktNieMusi(){
		throw new RException2();
	}

}
```
# Konstruktor wyjątku
Wyjątek zazwyczaj zawiera konstruktor bezargumentowy oraz konstruktor ze zmienną String.
```java
throw new Exception();
throw new Exception("Błąd!");
```
# Implementacja własnego wyjątku
```java
class ZeroWMacierzy extends RuntimeException {
	
}
```

# Działanie w Javie
1. Obiekt wyjątku tworzony na stercie.
2. Ścieżka egzekucji jest przerywana.
3. Referencja do wyjątku jest wyrzucana z kontekstu.
4. Mechanizm obsługi wyjątków szuka miejsca gdzie kontynuować, (`catch`)
