https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html
Klasa zawierające statyczne metody do działań na kolekacjach.
# Sortowanie
Klasa `Collections` zawiera statyczną metodę `sort` biorącą jako argumenty: 
- Listę
- Obiekt typu [[Comparator<T>]] (Jeżeli elementy listy nie implementują interfejsu `Comparable`)
Metoda domyślnie sortuje rosnąco. Aby odwrócić kolejność wystarczy odwrócić znak.
# Wyszukiwanie binarne
Klasa `Collections` zawiera statyczną metodę `binarySearch` wyszukującą klucz w liście.  Są 2 wersje:
- `binarySearch(Lista, klucz)` elementy listy muszą implementować `Comparable`
- `binarySerach(Lista, klucz, Comparator)`
Oba metody zwracają indeks. W przypadku nieznalezienia to $-1$.

> [!WARNING] UWAGA
> Lista musi być posortowana

# Odwracanie kolejności
Za pomocą metody statycznej `Collections.reverse(List)`
# Losowa kolejność
Za pomocą metody statycznej `Collections.shuffle(List, seed)` można zmienić kolejność na losową. seed jest opcjonalny.
# Zamień 2 elementy
`Collections.swap(List, a, b)`
# Wypełnij
`Collections.fill(List, obj)`
# Kopiuj
`Collections.copy(dst, src)`
# policz ile
`Collections.frequency(List, szukane)` zwraca int
# Minimum i Maksimum
2 podobne funkcje. Podobnie jak w przypadku sortowania i wyszukiwania binarnego elementy Listy muszą implementować `Comparable`, w przeciwnym razie konieczne jest podanie w argumencie instancji klasy implementującej interfejs `Comparator`

- `Collections.min(ListaObiektowComparable)`/ `Collections.min(Lista, ObiektComparator)`
- `Collections.max(ListaObiektowComparable)`/ `Collections.max(Lista, ObiektComparator)`

Powyższe metody zwracają **Obiekt** minimalny/maksymalny.