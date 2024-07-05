#AnalizaMatematyczna #Szeregi #SzeregGeometryczny 
# Ciąg geometryczny
$$
a_{n} = a_{n-1}*q
$$
lub 
$$
a_{n} = a_{b}*q^{n-b}
$$
gdzie $q$ - iloraz.
Iloraz $q$ można wyliczyć w następujący sposób:
$$
q = \frac{a_{n}}{a_{n-1}} 
$$
lub 
$$
q = \frac{a_{n+1}}{a_{n}}
$$
# Szereg geometryczny
Szereg geometryczny to taki szereg, który jest sumą wyrazów ciągu geometrycznego.
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