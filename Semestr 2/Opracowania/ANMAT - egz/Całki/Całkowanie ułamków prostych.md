# Całkowanie ułamków prostych
$$
\int \frac{f(x)}{g(x)} dx
$$
gdzie $f(x)$ i $g(x)$ to są wielomiany zmiennej $x$, oraz $f(x)$ jest mniejszego stopnia niż $g(x)$

## Rozkładanie mianownika na czynniki
**Ta metoda działa najlepiej, gdy stopień licznika jest o jeden mniejszy niż stopień mianownika**


Rozkładamy wielomian $g(x)$ na czynniki, w przypadku funkcji kwadratowej można obliczyć deltę. Trochę trudniej w przypadku wielomianu większego stopnia.

Następnie tworzymy ułamki których suma będzie równa naszemu ułamkowi.
Jeżeli stopień licznika jest o 1 mniejszy niż mianownika to łatwo.

W przypadku $\Delta = 0$ dzielimy na $\frac{A}{x - x_{0}}$ oraz $\frac{B}{(x - x_{0})^2}$
### Przykład
$$
\frac{x + 13}{(x+1)(x-5)} = \frac{A}{x+1} + \frac{B}{x-5}
$$
$$
A(x-5) + B(x+1) = x + 13
$$
$$
x(A + B) + (-5A + B) = x + 13
$$
$$
\begin{cases}
A + B = 1 \\
-5A + B = 13
\end{cases}
$$
Następnie liczymy $A$ i $B$, oraz podstawiamy do powyższych ułamków. Ułamki otrzymane można łatwo całkować.
### Przykład 2
$$
\frac{x + 3}{x^2 + 6x + 9} = \frac{A}{x+3} + \frac{B}{(x+3)^2}
$$
## Całkowanie funkcji wymiernych
Jeżeli $\Delta < 0$ nie można użyć wcześniejszej metody. Zamiast jej można użyć jednego z następujących wzorów. 
$$
\int \frac{g'(x)}{g(x)}dx = \ln|g(x)| + C
$$
Czasami da się rozłożyć całkę ułamku prostego w następujący sposób.
$$
\int \frac{2x + 3}{x^2 + 1} dx = \int \frac{2x}{x^2+ 1} dx + 3 \int\frac{1}{x^2 + 1} dx
$$
$$
\int \frac{2x}{x^2 + 1}dx = \ln|x^2 +1| + C
$$
$$
\int \frac{1}{x^2 + 1} dx= \arctan (x) +C
$$
## Twierdzenie Ostrogradskiego
$$

$$
![[Metody całkowania 2024-08-26 20.10.16.excalidraw|size=100%]]
Pod warunkiem, że $f(x)$ jest mniejszego stopnia niż $g(x)$.
### Przykład
$$
\begin{lgathered}


\int \frac{4x -2}{(x+2)^3} dx \\
f(x) = 4x - 2\\
g(x) = (x+2)^3\\ \\
\hline
g'(x) = 3(x+2)^2\\ \\

G(x) = (x+2)^2\\

W(x) = Ax + B\\ 

s(x) = \frac{g(x)}{G(x)} = \frac{(x+2)^3}{(x+2)^2} = x+2 \\
h(x) = C \\
\hline \\
\int \frac{4x-2}{(x+2)^3} dx = \frac{{Ax + B}}{(x+2)^2} + \int \frac{C}{x+2} dx
\end{lgathered}
$$
Następnie robimy pochodną obu stron równania w celu wyliczenia współczynników.

$$
\begin{lgathered}
\frac{4x-2}{(x+2)^3} = \left[ \frac{Ax+B}{(x+2)^2} \right]' + \frac{C}{x+2} \\
\frac{4x-2}{(x+2)^3} = \frac{A(x+2)^2 - (Ax+B)*2(x+2)}{(x+2)^4} + \frac{C}{x+2} \\

\end{lgathered}
$$
Współczynniki powinny wyjść następująco:
$$
\begin{cases}
C = 0 \\
A = -4  \\
B = -3
\end{cases}
$$
Więc ostatecznie całka po zastosowaniu twierdzenia Ostrogradskiego wygląda następująco:
$$
 \int \frac{4x-2}{(x+2)^3} dx = \frac{-4x - 3}{(x+2)^2} + \int 0 dx = \frac{-4x - 3}{(x+2)^2} + C
$$
