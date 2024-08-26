Całkowanie funkcji trygonometrycznych
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
