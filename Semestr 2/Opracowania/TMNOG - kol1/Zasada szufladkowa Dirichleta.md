Masz $n$ szufladek i $m$ osób. jeżeli aby udowodnić że przynajmniej $k$ osób należy do jednej szufladki wystarczy udowodnić, że $m < nk$ oraz $m > n * (k-1)$
# Przykład 1 - Ilość włosów
Jest $50,000$ ludzi który mają od $0$ do $40,000$  włosów, udowodnij że przynajmniej $2$ ludzie mają tyle samo włosów. 
- $k = 1: 40,000 * 1 < 50,000$
- $k = 2: 40,000 * 2 > 50,000$


# Przykład 2 - ilość kropek w sześcianie o boku 2
Masz ileś tam kropek w sześcianie o krawędzi 2, no i masz udowodnić że przynajmniej ileś z ich jest w odległości > $\sqrt{ 3 }$ od siebie.
No i dzielisz ten sześcian na 6 sześcianów o boku 1. W tym przypadku przekątna jest równa $\sqrt{ 3 }$ a bok $\sqrt{ 1 }$ więc i tak są zbliżone do siebie, ale to jeżeli kilka punktów będzie musiało znajdować się w sześcianach, to oznacza, że na pewno ileś z nich musi mieć $\sqrt{ 3 }$. Tutaj jest jakby takie przybliżenie i i tak części pewnie nie zauważa, ale jest wystarczające żeby udowodnić że przynjamniej tyle jest.

# Przykład 3 - Trójkąt
Tutaj pamiętam że dzieliliśmy trójkąt na małe trójkąty o takiej samej krawędzi. W tym przypadku najkrótsza droga pomiędzy 2 punktami które są blisko siebie to bok trójkąta. W tym przypadku bok trójkąta dajemy na większy niż odległość i jest.

# Wzory które mogą się przydać
## Koło
$$
P = \pi r^2
$$
$$
P = 2\pi r
$$
## Kula
$$
P = \frac{4}{3} \pi r^3
$$
$$
P = 4 \pi r^2
$$
# Ostrosłup
$$
P = \frac{1}{3} * P_{P}* H 
$$