#Całki #AnalizaMatematyczna
# Całkowanie przez części
Jeżeli funkcje mają ciągłe pochodne, to:
$$
\int (f(x) * g'(x))dx = f(x)*g(x) - \int f'(x)*g(x)
$$
lub odwrotnie
$$
\int (f'(x) * g(x)) = f(x)*g(x) - \int f(x)*g'(x)
$$
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
# Podstawienia Eulera
Całkę postaci 
$$ \int \frac{1}{\sqrt{ x^2 +k }} dx$$
gdzie $k$ to dowolna stała niezerowa, obliczamy stosując *podstawienie Eulera*.
Podstawienie Eulera wygląda następująco:
$$
t = x + \sqrt{ x^2 + k }
$$
$$
dt= 1 + \frac{x}{\sqrt{ x^2 + k }} dx = \frac{\sqrt{ x^2 +k } + x}{\sqrt{ x^2 +k }}dx = \frac{t}{\sqrt{ x^2 +k }}dx
$$
Zatem
$$
\frac{dt}{t} = \frac{1}{\sqrt{ x^2 +k }}dx
$$
A więc:
$$
\int \frac{1}{\sqrt{ x^2 +k }} dx = \int \frac{dt}{t} dx = \ln|t| + C = \ln |x + \sqrt{ x^2 +k }| + C
$$ 
# Całkowanie funkcji trygonometrycznych
## Podstawienie sinusowe
Stosujemy gdy $\cos$ jest w potędze nieparzystej. Albo, bardziej precyzyjnie: wtedy, gdy dla odpowiedniego $\cos$ funkcja zmienia znak.
$$
R(\cos x, \sin x) = -R(-\cos x, \sin x)
$$
$$
t = \sin x
$$
$$
dx = \frac{1}{\sqrt{1-t^2 }}
$$
$$
\cos x = \sqrt{ 1-t^2 }
$$

## Podstawienie cosinusowe
Stosujemy gdy $\sin$ jest w potędze nie parzystej. Albo, bardziej precyzyjnie: wtedy, gdy dla odpowiedniego $\sin$ funkcja zmienia znak.
$$
R(\cos x, \sin x) = -R(\cos x, -\sin x)
$$
$$
t = \cos x
$$
$$
dx = - \frac{1}{\sqrt{ 1-t^2 }} dt
$$
$$
\sin x = \sqrt{ 1-t^2 }
$$
## Podstawienie tangensowe
Stosujemy gdy sinus i cosinus mają parzyste potęgi. Albo, bardziej precyzyjnie funkcja ma ten sam znak nie zależnie od wartości $\sin/\cos$
$$
R(\cos x, \sin x) = R(-\cos x, -\sin x)
$$
$$
t = \tan x
$$
$$
x = \arctan(t)
$$
$$
dx = \frac{1}{1+t^2} dt
$$
$$
\cos ^2 (x) = \frac{1}{1+t^2}
$$
$$
\sin^2(x) = \frac{t^2}{1+t^2} 
$$
## Podstawienie uniwersalne (tangens połówkowy) 
Tutaj stosujemy podstawienia wynikające z znanych tożsamości trygnometrycznych.
Ta metoda jest uniwersalna, ale najlepiej jej używać wtedy gdy inne podstawienia trygonometryczne zawodzą.
$$
t = \tan \frac{x}{2}
$$
$$
x = 2\arctan(t)
$$
$$
dx = \frac{2}{1 +t^2} dt
$$
$$
\cos(x) = \frac{1- t^2}{1+t^2}
$$
$$
\sin(x) =  \frac{2t}{1+t^2}
$$
$$
\int R(\cos x, \sin x) dx = \int R\left( \frac{1-t^2}{1+t^2}, \frac{2t}{1+t^2} \right)  \frac{2}{1+t^2}dt
$$
