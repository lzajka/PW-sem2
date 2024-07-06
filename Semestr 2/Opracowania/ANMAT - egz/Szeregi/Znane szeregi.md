#AnalizaMatematyczna #Szeregi #Granice
# Szereg harmoniczny
Szereg postaci
$$
\sum_{n = 1}^\infty \frac{1}{n} = \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \dots
$$

## Rozbieżność
Szereg harmoniczny jest szeregiem rozbieżnym.
## Zastosowanie
Szereg harmoniczny znajduje często w sprawdzaniu zbieżności innych szeregów za pomocą [[Kryteria zbieżności#Kryterium porównawcze|kryteria porównawczego]] 
# Szereg anharmoniczny
To jakby połączenie szeregu harmonicznego oraz szeregu naprzemiennego.
$$
\sum_{n = 1}^\infty \frac{1}{n} (-1)^{n+1}
$$
# Szeregi Dirichleta
Dowolny szereg postaci
$$
\sum_{n = 1}^\infty \frac{1}{n^\alpha}
$$
Szereg takiej postaci:
- Jest **zbieżny** dla $\alpha > 1$
- Jest **rozbieżny** dla $\alpha \leq 1$

# Szereg potęgowy
# Szereg geometryczny
Szereg geometryczny to taki szereg, który jest sumą wyrazów [[Ciąg geometryczny|ciągu geometrycznego]].
Ogólnie to można go zapisać w takiej postaci.
$$
\sum_{n=1}^\infty a_{1}q^{n-1}
$$
## Wartość sumy $n$-elementowej
Dla $q \neq 1$: $S_{n} = \frac{1 - q^n}{1 - q}$
Dla $q = 1$: $S_{n} = na$ (wartości ciągu są takie same.)

## Warunek zbieżności szeregu geometrycznego.
Jeżeli $|q| < 1$ lub $a = 0$ to szereg jest zbieżny.
Spełnienie tego warunku konieczne jest do obliczenia wartości szeregu.
## Suma wszystkich elementów
$$
\sum_{n = 1}^\infty a_{n_{1}} q^{n-1} = \frac{a_{1}}{1 - q}
$$
# Szereg potęgowy
Jest to szereg postaci:
$$
\sum_{n = 1}^\infty a_{n}(x - x_{0})^n
$$
gdzie, $a_{n} \neq 0$ dla $n \in \mathbb{N}$, $x \in \mathbb{R}$
oraz $x_{0}$ jest to środek szeregu.
## Obszar zbieżności
Polega na znalezieniu wartości $x$ dla której szereg jest zbieżny.
Szereg zawsze jest zbieżny w przypadku w którym $x = x_{0}$.
## Zbieżność na krańcach