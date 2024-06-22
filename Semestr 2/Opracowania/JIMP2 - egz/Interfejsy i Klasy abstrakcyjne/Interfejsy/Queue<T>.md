W przeciwieństwie do Stosu kolejka jest interfejsem. Konieczne metody do zaimplementowania to:
- `void add(T element)` - Dodaje nowy element na koniec kolejki.
- `E element()` - Zwraca pierwszy element w kolejce.
- `boolean offer(T element)` - Dodaje nowy element na koniec kolejki, jeżeli nie wymusi zwiększenia rozmiaru.
- `E peek()` - To samo co `element`, tylko że gdy nie ma to zwraca `Null`a
- `E poll()` - Zwraca i usuwa, jeżeli pusta zwraca `Null`a
- `E remove()` - Usuwa element.
# Znane implementacje
- `Dequeue`
- `PriorityQueue`
- `LinkedList`