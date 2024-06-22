# hashCode
Funkcja typu int zwracająca hasz, przydatna do indeksowania elementów w między innymi mapach.
```
@Override
public int hashCode(){
	return 0;
}
```
# equals
Funkcja boolowska porównująca elementy.
```
@Override
public boolean equals(Object o)
```
1. Najpierw sprawdzamy czy elementy są takiego samego typu
	`if (!(o instanceof ObiektPorównywany)) return false;`
2. Następnie castujemy
   `ObiektPorównywany op = (ObiektPorównywany) o;`
3. Ostatnim krokiem jest porównanie wartości zmiennych. Ponieważ oba obiekty są instancjami tej samej klasy, jest możliwość porównywania zmiennych prywatnych bezpośrednio.
# toString
Funkcja konwertująca zmienną na postać tekstową. 
```
@Override
public String toString(){
...
}
```
