#AnalizaMatematyczna #Pochodne #FunkcjeWieluZmiennych #Monotoniczność #AnalizaFunkcji

# Warunek konieczny istnienia ekstremów
Jeśli funkcja $f(P) = f(x_{1}, x_{2},\dots, x_{n})$ posiada pochodną cząstkową rzędu pierwszego w punkcie $P_{0}$ ma w tym punkcie ekstremum lokalne, gdy:
$$
\forall_{i = 1, \dots, n} \frac{\partial f}{\partial x_{i}} (P_{0}) = 0
$$
## Interpretacja
Czyli, jeżeli pochodna cząstkowa dla pewnego punktu po każdej zmiennej jest równa $0$, to w tym miejscu **może** być ekstremum.


# Warunek dostateczny istnienia ekstremum (2 zmienne)
Jeżeli:
- Funkcja jest klasy $C^2$ na pewnym otoczeniu punktu $P$ (pochodna cząstkowa 2 rzędu jest ciągła)
- $f'_{x}(P) = f'_{y}(P) = 0$
- $\det(H) > 0$
- $\delta = [f''_{xy}(P)]^2 - f''_{xx}(P)*f''_{yy}(P) < 0$
To w punkcie P ma:
- Minimum    jeżeli $f''_{xx}(P) > 0$ oraz $f''_{yy}(P) > 0$
- Maksimum jeżeli $f''_{xx}(P) < 0$ oraz $f''_{yy}(P) < 0$

> [!Warning] Ewentualnie może zdarzyć się tak, że pomimo $\delta = 0$ jest ekstremum.
> Wtedy jest przypadek nieokreślony (wątpliwy)
## Macierz Hessego (H)
$$
H = \begin{bmatrix}
7
\end{bmatrix}
$$