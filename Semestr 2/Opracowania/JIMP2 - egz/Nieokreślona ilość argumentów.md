Można stworzyć metodę która bierze tyle argumentów ile jest ich podane.

## Fragment kodu
```java
public void printAll(String ... strings) {
	for(String string : strings) {
		System.out.println(string);
	}
}
```