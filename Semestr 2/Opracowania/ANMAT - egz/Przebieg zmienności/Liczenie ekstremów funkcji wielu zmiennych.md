#AnalizaMatematyczna #Pochodne #FunkcjeWieluZmiennych #Monotoniczność #AnalizaFunkcji

# Warunek konieczny istnienia ekstremów
Jeśli funkcja $f(P) = f(x_{1}, x_{2},\dots, x_{n})$ posiada pochodną cząstkową rzędu pierwszego w punkcie $P_{0}$ ma w tym punkcie ekstremum lokalne, gdy:
$$
\forall_{i = 1, \dots, n} \frac{\partial f}{\partial x_{i}} (P_{0}) = 0
$$
## Interpretacja
Czyli, jeżeli pochodna cząstkowa dla pewnego punktu po każdej zmiennej jest równa $0$, to w tym miejscu **może** być ekstremum.

# Macierz Hessego ($H$)
Macierz wykorzystywana podczas znajdowania ekstremów.
Zawiera pochodne cząstkowe 2 rzędu funkcji.
$$
H(P) = \begin{bmatrix}
\frac{ \partial^2 f}{ \partial x_{1} \partial x_{1}}(P) & \frac{ \partial^2 f }{ \partial x_{1} \partial x_{2} }(P) & \frac{ \partial ^2 f }{ \partial x_{1} \partial x_{3} }(P)  & \dots & \frac{ \partial^2 f }{ \partial x_{1} \partial x_{n} }(P)    \\
\frac{ \partial ^2f }{ \partial x_{2} \partial x_{1} }(P)  & \frac{ \partial ^2 f }{ \partial x_{2} \partial x_{2} }(P)  & \frac{ \partial ^2 f }{ \partial x_{2} \partial x_{3} }(P)  & \dots & \frac{ \partial ^2 f }{ \partial x_{2}\partial x_{n} }(P)  \\
\frac{ \partial ^2 f }{ \partial x_{3} \partial x_{1} }(P) & \frac{ \partial ^2 f }{ \partial x_{3} \partial x_{2} }(P)  & \frac{ \partial ^2 f }{ \partial x_{3} \partial x_{3} }(P)  & \dots & \frac{ \partial ^2 f }{ \partial x_{3} \partial x_{n} }(P)  \\
\dots & \dots & \dots & \dots & \dots \\
\frac{ \partial ^2 f }{ \partial x_{n} \partial x_{1} }(P)  & \frac{ \partial ^2f }{ \partial x_{n} \partial x_{2} }(P)  & \frac{ \partial ^2 f }{ \partial x_{n} \partial x_{3} }(P)  & \dots & \frac{ \partial ^2 f }{ \partial x_{n} \partial x_{n} }(P)   
\end{bmatrix}

$$
## Minory główne
Minory główne $A_{n}$ są to wyznaczniki fragmentu macierzy Hessego o wymiarach $n \times n$ rozpoczynając od lewego górnego rogu
### Przykład
$$
A_{1}(P) = \frac{ \partial ^2 f }{ \partial x_{1} \partial x_{1} } 
$$
$$
A_{2}(P) = \begin{vmatrix}
\frac{ \partial^2 f}{ \partial x_{1} \partial x_{1}}(P) & \frac{ \partial^2 f }{ \partial x_{1} \partial x_{2} }(P)   \\
\frac{ \partial ^2f }{ \partial x_{2} \partial x_{1} }(P)  & \frac{ \partial ^2 f }{ \partial x_{2} \partial x_{2} }(P)   \\

\end{vmatrix}
$$
$$
A_{3}(P) = \begin{vmatrix}
\frac{ \partial^2 f}{ \partial x_{1} \partial x_{1}}(P) & \frac{ \partial^2 f }{ \partial x_{1} \partial x_{2} }(P) & \frac{ \partial ^2 f }{ \partial x_{1} \partial x_{3} }(P) \\
\frac{ \partial ^2f }{ \partial x_{2} \partial x_{1} }(P)  & \frac{ \partial ^2 f }{ \partial x_{2} \partial x_{2} }(P)  & \frac{ \partial ^2 f }{ \partial x_{2} \partial x_{3} }(P) \\
\frac{ \partial ^2 f }{ \partial x_{3} \partial x_{1} }(P) & \frac{ \partial ^2 f }{ \partial x_{3} \partial x_{2} }(P)  & \frac{ \partial ^2 f }{ \partial x_{3} \partial x_{3} }(P)
\end{vmatrix}
$$

## Określoność
1. Gdy wszystkie minory główne są dodatnie - **Minimum lokalne**
2. Gdy wszystkie minory główne zmieniają znak, zaczynając od minusa - **Maksimum lokalne**
3. Jeżeli $A_{2}(P) = 0$ - **Nie wiadomo**
4. Jeżeli $A_{2}(P) < 0$ - **Macierz nieokreślona**
# Warunek dostateczny istnienia ekstremum (2 zmienne)
Jeżeli:
- Funkcja jest klasy $C^2$ na pewnym otoczeniu punktu $P$ (pochodna cząstkowa 2 rzędu jest ciągła)
- $f'_{x}(P) = f'_{y}(P) = 0$ ([[#Warunek konieczny istnienia ekstremów]])
- $\det(H) > 0$
To w punkcie $P$ mamy *ekstremum lokalne*.
Jeżeli:
- $f''_{xx}(P) > 0$ - **Minimum lokalne**
- $f''_{xx}(P) < 0$ - **Maksimum lokalne**

> [!Warning] Ewentualnie może zdarzyć się tak, że pomimo $\det(H) = 0$ jest ekstremum.
> Wtedy jest przypadek nieokreślony (wątpliwy)
# Warunek dostateczny istnienia ekstremum (więcej zmiennych)
Jeżeli:
- Funkcja jest klasy $C^2$ na pewnym otoczeniu punktu $P$ (pochodna cząstkowa 2 rzędu jest ciągła)
- Każda pochodna 1 stopnia jest równa $0$ ([[#Warunek konieczny istnienia ekstremów]])
- [[#Macierz Hessego ($H$)|Macierz Hessego]] jest określona 
