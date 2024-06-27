
# Czytanie 
## za pomocą `Scanner`
### Importy
```java
import java.io.File;
import java.util.Scanner;
```
### Czytanie z pliku
```java
File f = new File("plik.txt", "r")
Scanner scanner = new Scanner(f);
```
### Czytanie z wejścia
```java
Scanner scanner = new Scanner(System.in);
```
### Czytanie całej linii
```java
// Sprawdzamy czy istnieje następna linia
while(scanner.hasNextLine()) {
	// Czyta linie. Za każdym kolejnym wywołaniem będzie przechodziło do kolejnej linii.
	String line = scanner.nextLine();

}
```

### Czytanie wartości określonego typu
Obiekt skanera zawiera metody umożliwiające czytanie [[Obiekty i Typy prymitywne#Typ prymitywny|zmiennych typu prymitywnego]], przed przeczytaniem należy sprawdzić czy dana wartość jest obecna.
#### Metody sprawdzające
- `boolean hasNextBoolean()`
- `boolean hasNextByte()`
- `boolean hasNextDouble()`
- `boolean hasNextFloat()`
- `boolean hasNextInt()`
- `boolean hasNextLong()`
- `boolean hasNextShort()`
- `boolean hasNext()`
#### Metody pobierające
- `boolean nextBoolean()`
- `byte nextByte()`
- `double nextDouble()`
- `float nextFloat()`
- `int nextInt()`
- `long nextLong()`
- `short nextShort()`
- `char next()`
### Zamykanie pliku
```java
scanner.close();
```

## Czytanie za pomocą `BufferedReader`
# Pisanie do pliku 
## Za pomocą`BufferedWriter`
### Importy
```java
import java.io.File;
import java.io.BufferedWriter;
```

### Przykład
```java
try {
	BufferedWriter writer = new BufferedWriter(new File("plik.txt", "w"));
	writer.write("Hello");
	writer.close(); 
} 
catch(IOException ex) {
	ex.printStackTrace();
}
```