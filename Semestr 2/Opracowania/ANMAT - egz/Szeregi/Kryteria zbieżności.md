#Granice #Szeregi #AnalizaMatematyczna #ZbieżnośćSzeregu
Kryteria zbieżności pomagają w określeniu czy dany szereg jest zbieżny, czy rozbieżny.

> [!WARNING] UWAGA
> W większości przypadków (prawie) wszystkie elementy ciągów są nieujemne.
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
Jeżeli od pewnego $n$ : $a_{n} > 0$ oraz $\lim_{ n \to \infty } \sqrt[n]{ |a_{n}|} = q$ to dla:
- $q < 1$: szereg jest zbieżny
- $q > 1$: szereg jest rozbieżny
- $q = 1$: zła metoda
## Rozszerzenie kryterium Cauchy'ego
Jeżeli od pewnego momentu $q \geq 1$ to szereg jest rozbieżny. 
# Kryterium (silne) d'Alamberta
$$
q = \lim_{ n \to \infty } | \frac{a_{n+1}}{a_{n}} | 
$$
- dla $q < 1$ - Szereg jest zbieżnych
- dla $q > 1$ - Szereg jest rozbieżny
- dla $q=1$ - Zła metoda 
## Rozszerzenie kryterium d'Alamberta
Jeżeli od pewnego momentu $q \geq 1$ to szereg jest rozbieżny.
# Kryterium ilorazowe
$$
g = \lim_{ n \to \infty } \frac{a_{n}}{b_{n}}
$$
- Jeżeli $0 < q < \infty$ oba szeregi są zarówno zbieżne lub rozbieżne
- Jeżeli $q = 0$ ze zbieżności $b_{n}$ wynika zbieżność $a_{n}$ i na odwrót
- Jeżeli $q = \infty$ z rozbieżności $b_{n}$ wynika rozbieżność $a_{n}$ i n a odwrót
# Kryterium Leibniza
Kryterium Leibniza jest przydatne w przypadku szeregów naprzemiennych (takich że znak zmienia się dla każdego elementu ciągu. Szereg naprzemienny zapisuje się w następującej postaci.
$$
\sum_{n = 1}^\infty (-1)^{n+1} a_{n}
$$
Twierdzenie mówi, że jeśli ciąg $a_{n}$ jest **nierosnący** i dążący do $0$, to szereg jest zbieżny.

> [!WARNING] Nie spełnienie kryterium rozbieżności szeregu.
# Zbieżność bezwzględna
![[Zbieżność warunkowa i bezwzględna#Zbieżność bezwzględna]]
