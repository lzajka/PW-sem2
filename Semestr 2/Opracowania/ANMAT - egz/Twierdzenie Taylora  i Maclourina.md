#AnalizaMatematyczna #TwierdzenieTaylora #Funkcje #WzórMaclourina #WzórTaylora
# Idea
W celu przybliżenia wartości funkcji trudnych do obliczenia można wykorzystać twierdzenie Taylora.
Mówi ono, że można zbliżyć taką funkcję do wielomianu $n$-tego stopnia. Tym większy stopień wielomianu, tym większa precyzja.
# Założenia
Funkcja ($n - 1$) różniczkowalna na jakimś przedziale $<a, b>$.
Oraz istnieje $n$-tego rzędu na przedziale $(a,b)$


# Wzór Taylora
$$
f(x) = \sum^{n-1}_{k=0} \frac{f^{(k)}(x_{0})}{k!}(x - x_{0})^k + \underbrace{ \frac{f^{(n)}(c)}{n!}(x - x_{0})^n}_{\text{Reszta Taylora } R_{n}(c) }
$$
$x_{0}$ powinno być jak najbliżej obliczanego $x$ oraz łatwe do obliczenia. 
*Reszta Taylora* - Służy do określenia dokładności aproksymacji. $c$ $\in (x, x_{0})$.
Zostawiamy $c$ podobnie jak $C$ w przypadku całek.
Błąd będzie się mieścił między $R_{n}(x)$ a $R_{n}(x_{0})$

## Przykład
$$
f(x) = e^x
$$
Maksymalna dokładność: 5
<iframe 
		src="https://www.desmos.com/calculator/zx0uoekwqh"
		height=1000px
		width=100%
		/>
# Wzór Maclourina ($x_{0} = 0$)
$$
f(x) = \sum^{n-1}_{k=0} \frac{f^{(k)}(0)}{k!} x^k + \frac{f^{(n)}(c)}{n!} * x^n
$$