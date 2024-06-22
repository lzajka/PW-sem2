# Sortowanie
Klasa `Collections` zawiera statyczną metodę `sort` biorącą jako argumenty: 
- Lista
- [[Comparator<T>]] (Chyba że elementy Listy są `Comparable`)
Metoda domyślnie sortuje rosnąco. Aby odwrócić kolejność wystarczy odwrócić znak.
# Wyszukiwanie binarne
Klasa `Collections` zawiera statyczną metodę `binarySearch`.  Są 2 wersje:
- `binarySearch(Lista, klucz)` elementy listy muszą implementować `Comparable`
- `binarySerach(Lista, klucz, Comparator)`
Oba metody zwracają indeks. W przypadku nieznalezienia to $-1$.

> [!WARNING] UWAGA
> Lista musi być posortowana

# Odwracanie kolejności
Za pomocą metody statycznej `reverse(List)`
# Losowa kolejność
Za pomocą metody statycznej `shuffle(List, seed)` można zmienić kolejność na losową. seed jest opcjonalny.
# Zamień 2 elementy
`swap(List, a, b)`
# Wypełnij
`fill(List, obj)`
# Kopiuj
`copy(dst, src)`
# policz ile
`frequency(List, szukane)` zwraca int
# Minimum i Maksimum
2 podobne funkcje. Podobnie jak w przypadku sortowania i wyszukiwania binarnego Elementy Listy muszą implementować `Comparable`, w przeciwnym razie konieczne jest podanie w argumencie instancji klasy implementującej interfejs `Comparator`