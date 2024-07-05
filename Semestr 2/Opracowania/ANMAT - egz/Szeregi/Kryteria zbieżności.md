#Granice #Szeregi #AnalizaMatematyczna 
Kryteria zbieżności pomagają w określeniu czy dany szereg jest zbieżny, czy rozbieżny.
# Warunek konieczny
Warunkiem koniecznym zbieżności szeregu jest taki że dla szeregu:
$$
\sum_{n = 1}^\infty a_{n},\text{         } \lim_{ n \to \infty } a_{n} = 0
$$
# Kryterium porównawcze
Jeżeli mamy 2 szeregi $\sum_{n = 1}^\infty a_{n}$ oraz $\sum^\infty_{n=1}b_{n}$, jeżeli od pewnego n zachodzą takie warunki: $0 \leq a_{n} \leq b_{n}$ to:

- Jeśli $\sum_{n = 1}^\infty a_{n}$ jest rozbieżny to  $\sum_{n = 1} ^\infty  b_{n}$ też jest rozbieżny.

- Jeśli $\sum_{n = 1}^\infty b_{n}$ jest zbieżny to $\sum_{n = 1} ^\infty a_{n}$ też jest zbieżny.
# Kryterium Couchy'ego
Jeżeli od pewnego $n$ : $a_{n} > 0$ oraz $\lim_{ n \to \infty } \sqrt[n]{ a_{n}} = q$ to dla:
- $q < 1$: szereg jest zbieżny
- $q > 1$: szereg jest rozbieżny
- $q = 1$: zła metoda
# Kryterium (silne) d'Alamberta
$$
g = \lim_{ n \to \infty } | \frac{a_{n+1}}{a_{n}} | 
$$
- dla $g < 1$  - Szereg jest zbieżnych
- dla $g > 1$ -  Szereg jest rozbieżny