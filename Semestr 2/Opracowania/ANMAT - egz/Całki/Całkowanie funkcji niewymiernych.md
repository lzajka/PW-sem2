
# 1
$$
\int \frac{1}{\sqrt{ 1-x^2 }} dx = \arcsin(x) + C
$$
# 2
$$
\int \frac{W(x)}{\sqrt{ ax^2 +bx + c }} dx = G(x) \sqrt{ ax^2 +bx + c } + K\int \frac{1}{\sqrt{ ax^2 +bx + c }}
$$
Współczynniki wyliczamy licząc pochodne każdej strony.
# Jakieś tam podstawienie
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
# Podstawienia Eulera 
Przydatne są w przypadku obliczania całek funkcji w postaci $R(ax^2 + bx + c)$ gdzie $R$ jest funkcją wymierną
## 1 Podstawienie Eulera ($a > 0$)
$$
\sqrt{ ax^2 + bx + c } = (t-x) \sqrt{ a }
$$
## 2 Podstawienie Eulera ($a < 0$ i $\Delta > 0$)
$$
\sqrt{ ax^2 + bx + c } = \left( x + \frac{b}{2a} \right)t - \sqrt{ - \frac{\Delta}{4a} }
$$
## 3 (?) Podstawienie Eulera ($a > 0$)
$$
\sqrt{ ax^2 + bx + c  } = t \pm x \sqrt{  a }
$$
## Przykład
![[Całkowanie funkcji niewymiernych 2024-08-26 22.57.40.excalidraw|size=100%]]
## 2