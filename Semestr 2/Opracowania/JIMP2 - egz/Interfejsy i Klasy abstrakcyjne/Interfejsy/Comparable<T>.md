Interfejs `Comparable` umożliwia porównywanie obiektów (mniejszy, większy lub równy). Umożliwia między innymi sortowanie elementów.
# compareTo
`int compareTo(T other)` metoda służy do porównywania elementów.
`a.compareTo(b)` zwraca:

| wartość | kiedy?  |
| ------- | ------- |
| $< 0$   | $a < b$ |
| $=0$    | $a=b$   |
| $>0$    | $a > b$ |

# Przykład

```java
class Player implements Comparable<Player> {
	private points;
	@Override
	int compareTo(Player otherPlayer){
		if(this.points < otherPlayer.points) return -1;
		else if(this.points == otherPlayer.points) return 0;
		else if(this.points > otherPlayer.points) return 1;
		else throw new Exception("How??!!!");
	}
}
```