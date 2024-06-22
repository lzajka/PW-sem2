# Pochodna cząstkowa
Zapis pochodnej cząstkowej funkcji $f$ po zmiennej $x_{1}$ wgląda następująco: $f'_{x_{1}}(\dots)$
Alternatywnie:
$$
\frac{\partial f}{\partial x_{1}}
$$
# Różniczka zupełna funkcji $f(x_{1}, \dots, x_{n})$ w punkcie $P_{0}$
$$
(df)_{P_{0}} = \frac{ \partial f }{ \partial x_{1} } (P_{0})dx_{1} + \frac{ \partial f }{ \partial x_{2} } (P_{0})dx_{2} + \dots + \frac{ \partial f }{ \partial x_{3} } (P_{0})dx_{3}
$$
# Forma kwadratowa
## Przykład
$$
f(x, y) = 3x^2 + 2xy + 4y^2
$$
## Zapis ogólny
$$
f(x_{1}, \dots, x_{n}) = \sum_{i, j = 1}^n a_{ij} x_{i} x_{j}
$$
TLDR: mnożysz każdą parę przez siebię, i jakieś a. 
Jak widać każda para wystąpi 2 razy w odwróconej kolejnośći.
Oczywiście macierz $A = [a_{ij}]_{n\times n}$ jest symetryczna ($a_{ij} = a_{ji}$)


## Kryterium określoniowości formy kwadratowej
1. Wyznaczamy wszystkie wyznacz $n \times n$ wyznaczamy $n$ wyznaczników macierzy, zaczynając od macierzy o wymiarze $1 \times 1$ do $n \times n$
## Dodatniość/ujemność
- Forma kwadratowa jest *dodatnio określona* wtedy, gdy zawsze z wyjątkiem przypadku w którym wszystkie argumenty są $0$ wartość funkcji jest dodatnia.
- Analogicznie jest w przypadku funkcji kwadratowej *ujemnie określonej*.
- W przeciwnym wypadku jest ona *nieokreślona*

### Na deltach
- Jeżeli wszystkie $\Delta$ są $> 0$ to forma kwadratowa jest $dodatnia$
- Jeżeli wszystkie $\Delta$ są naprzemienne, zaczynając od 1 $< 0$ to forma kwadratowa jest *ujemna*
- W przeciwnym wypadku jest ona *nieokreślona*
## Druga różniczka funkcji
Po prostu zróżniczkuj różniczkę.
# Macierz Hessego
To jest macierz pochodnych 2 rzędu. gdzie kolumny reprezentują pierwszą pochodną, a wiersze 2 pochodną (albo na odwrót)
$$
H(x_{0}) = \begin{bmatrix}
\frac{ \partial^2 f }{ \partial x_{1}^2 }(x_{0}) &  \frac{ \partial^2 f }{ \partial x_{1} \partial x_{2} }(x_{0}) & \dots  &  \frac{ \partial^2 f }{ \partial x_{1} \partial x_{n} }(x_{0}) \\
\frac{ \partial^2 f }{ \partial x_{2} \partial x_{1} }(x_{0}) &  \frac{ \partial^2 f }{ \partial x_{2} \partial x_{2} }(x_{0}) & \dots  &  \frac{ \partial^2 f }{ \partial x_{2} \partial x_{n} }(x_{0}) \\
\dots & \dots & \dots & \dots \\
\frac{ \partial^2 f }{ \partial x_{n} \partial x_{1} }(x_{0}) &  \frac{ \partial^2 f }{ \partial x_{n} \partial x_{2} }(x_{0}) & \dots  &  \frac{ \partial^2 f }{ \partial x_{n} \partial x_{n} }(x_{0})
\end{bmatrix}
$$


# Ekstrema funkcji 
## Warunek koniczny istnienia ekstremum klasy $C_{1}$ w punkcie $P_{0}$
1. Wszystkie pochodne cząstkowe pierwszego stopnia się zerują w punkcie $P_{0}$ (Punkt ten nazywa się *punktem stacjonarnym*)
2. Jedynie w *punkcie stacjonarnym* mogą wstępować minima/maksima lokalne.
## 1 Warunek konieczny istnienia ekstremum  klasy $C_{2}$ w punkcie $P_{0}$
1. W punkcie $P_{0}$ wszystkie różniczki częściowe są równe 0
2. Druga różniczka w punkcie $P_{0}$ jest określona.
Wtedy: 
- Minimum lokalne gdy: $(d^2 f)_{P_{0}} > 0$
- Maksimum lokalne gdy: $(d^2 f)_{P_{0}} < 0$
## 2 Warunek konieczny istnienia ekstremum  klasy $C_{2}$ w punkcie $P_{0}$ (Dla funkcji 2 zmiennych)
1. W punkcie $P_{0}$ wszystkie różniczki częściowe są równe 0
2. $|H(P_0)| > 0$
Wtedy:
- minimum lokalne gdy: $f''_{xx} > 0$
- maksimum lokalne gdy: $f''_{x x} < 0$
