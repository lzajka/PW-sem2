# Importy
```java
import java.io.*;
import java.util.Scanner;
```
# Czytanie z pliku
```java
File f = new File("plik.txt", "r")
Scanner scanner = new Scanner(f);

while(scanner.has)
```
# Pisanie do pliku
## `BufferedWriter`
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