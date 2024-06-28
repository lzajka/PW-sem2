https://docs.oracle.com/javase/8/docs/api/java/util/Map.html
Taka jakby tablica, tylko, że indeksy (tutaj klucze) nie muszą być wartością prymitywną `int`, ale mogą być obiektami
> [!WARNING] UWAGA
> Podobnie jak w przypadku zbiorów elementy mapy muszą odpowiednio przesłonić metodę `boolean equals(Object o)`

# Podstawowe typy
 [[Set<T>#Wbudowane implementacje]] praktycznie to samo, tyle że zamiast `Set` jest `Map`
 
metody:
- `put(T1 klucz, T2 wartość)`
- `T2 get(T1 klucz)`
- `boolean containsKey(T1 klucz)` - sprawdza czy istnieje taki klucz
- `containsValue(T2 value)` - sprawdza czy taka wartość 
- `keySet()` - Zwraca zbiór kluczy
# Przykład

```java
import java.util.HashMap;
public class Main {
	public static void main(String[] args) {
		HashMap<Student, Grade> ocenyStudentow = new HashMap<>();
		Student jk = new Student("Janusz Kowalski");
		ocenyStudentow.put(jk, new Grade(3));
		ocenyStudentow.put(new Student("Mateusz"), new Grade(4));

		Grade ocenaJanusza = ocenyStudentow.get();
		// W podanym przypadku jeżeli założymy że metoda haszująca i equals będzie działała po nazwie studenta to ocena Mateusza to będzie 4.
		// Gdyby było hashCode oraz equals było domyślne, to nie bo działa po adresie pamięci.
		Grade ocenaMateusza = ocenyStudentow.get(new Student("Mateusz"));


	}

}

```