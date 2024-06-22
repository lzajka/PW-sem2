# Jak zaimportować
Można zaimportować za pomocą `java.util.Random`, albo `java.util.*`
# Konstruktor
Klasa zawiera 2 konstruktory. 
1. `Random()`, ziarno jest losowe
2. `Random(long seed)`
# Generowanie losowej liczby całkowitej
`randomInt(bound)`, zwraca losową liczbę całkowitą od $0$ (włączając), do `bound` (wyłączając)

`randomInt()` zwraca losową liczbę całkowitą od $0$

# Generowanie ułamków
`nextFloat()` oraz `nextDouble()` zwraca ułamek, od $0.0$ do $1.0$. Każdy ułamek ma tą samą szansę.

`nextGaussian()` zwraca ułamek od $0.0$ do $1.0$, według krzywej Gaussa.

# Ustawianie ziarna
Ziarno może być ustawione za pomocą metody `setSeed(long)`