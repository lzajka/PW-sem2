https://docs.oracle.com/javase/8/docs/api/java/util/Set.html
Inteferjs określający zbiór elementów. W takim zbiorze elementy nie mogą się powtarzać. 
Znajduje się w `java.util.Set`

Z reguły obiekty które będą używane w `Set` muszą posiadać odpowiednio [[Przeciążenie i Przesłonięcie|przesłoniętą]] metodę `boolean equals(Object o)`
# Wbudowane implementacje
https://docs.oracle.com/javase/tutorial/collections/implementations/set.html
Ponieważ `Set<>` jest interfejsem konieczne jest zastosowanie implementacji.
W poniższej tabeli pokazane są najprzydatniejsze implementacje interfejsu `Set<>`.

| Implementacja   | Czas wstawiania                    | Czas przesukiwania                 | Kiedy warto?                                                                                                     | Wymagania                                    | Kolejność                            |
| --------------- | ---------------------------------- | ---------------------------------- | ---------------------------------------------------------------------------------------------------------------- | -------------------------------------------- | ------------------------------------ |
| `HashSet`       | Praktycznie natychmiastowa.        | Praktycznie natchmiastowa.         | Jeżeli nie trzeba wykorzystać innej.                                                                             | odpowiednio przesłonięta metoda `hashCode()` | Brak                                 |
| `TreeSet`       | Czas logarytmiczny.                | Czas logarytmiczny.                | Potrzebne jest posiadanie elementów w posortowanej kolejności lub kiedy chcemy wykorzystać interfejs `SortedSet` | implementacja `Comparable`                   | Rosnąca                              |
| `LinkedHashSet` | Delikatnie wolniejsza od `HashSet` | Delikatnie wolniejsza od `HashSet` | Potrzebne jest posortowanie elementów według wstawienia.                                                         | odpowiednio przesłonięta metoda `hashCode()` | Wstawienia (najstarszy -> najnowszy) |

# Podstawowe metody określone przez interfejs
- `boolean add(E e)` - Dodaje element do zbioru. W przypadku w którym on już się tam znajduje zwraca `false`, w przeciwnym wypadku `true` .
- `boolean remove(Object o)` - Usuwa elementy który jest taki sam jak element `o`.
- `boolean contains(Object o)` - Czy zbiór zawiera obiekt o?
- `boolan isEmpty()` - Czy zbiór jest pusty?
- `boolean equals(Object o)` - Porównuje 
> [!WARNING] UWAGA
> To są najprzydatniejsze metody określone przez interfejs `Set<>`. Implementacja interfejsu `Set` wymaga zdefiniowania większej ilości metod.

# Collection
Interfejs `Set` dziedziczy z `Collection`. Klasa [[Collections]] zawiera przydatne metody działające na obiektach `Collection`.
## Tworzenie nowego `Set` na podsawie `Collection`
Z reguły implementacje klasy `Set` posiadają [[Przeciążenie i Przesłonięcie#Przeciążenia|przeciążenie]] konstruktora zawierające argument `Collection`, umożliwiający utworzenie nowego zbioru na podstawie zawartości kolekcji.
### Przykład
```java
ArrayList<Student> students = new ArrayList<>();
//...
HashSet<Student> studentSet = new HashSet<>(studentList)
```
Na podstawie elementów z Listy `students` zostanie utworzony nowy zbiór `studentSet`
## Tworzenie nowego `Collection` na podstawie `Set`
Podobnie można w przeciwną stronę dla klas posiadających w konstruktorze argument `Collection`.
```java

HashSet<Student> studentSet = new HashSet<>()
// ...
ArrayList<Student> students = new ArrayList<>(studentSet);
```

## Tworzenie nowego `Set` na podstawie innego `Set`
Ponieważ `Set` dziedziczy z `Collection` można utworzyć nowy `Set` na podstawie innego.

```java
HashSet<Student> studentSet1 = new HashSet<>();
/// ...
TreeSet<Student> studentSet2 = new StudentSet<>(studentSet1);
```
