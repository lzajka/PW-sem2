#AnalizaMatematyczna #TwierdzenieTaylora #Funkcje #WzórMaclourina #WzórTaylora
# Idea
W celu przybliżenia wartości funkcji trudnych do obliczenia można wykorzystać twierdzenie Taylora.
Mówi ono, że można zbliżyć taką funkcję do wielomianu $n$-tego stopnia. Tym większy stopień wielomianu, tym większa precyzja.
# Założenia
Funkcja ($n + 1$) różniczkowalna na jakimś przedziale.

# Wzór Taylora
$$
f(x) = \sum^{n-1}_{k=0} \frac{f^{(k)}(x_{0})}{k!}(x - x_{0})^k + \underbrace{ \frac{f^{(n)}(c)}{n!}(x - x_{0})^n}_{\text{Reszta Taylora } R_{n}(c) }
$$
# Wzór Maclourina ($x_{0} = 0$)
$$
f(x) = \sum^{n-1}_{k=0} \frac{f^{(k)}(0)}{k!} x^k + \frac{f^{(n)}(c)}{n!} * x^n
$$