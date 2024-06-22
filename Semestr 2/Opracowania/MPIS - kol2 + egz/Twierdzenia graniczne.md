# Integralne twierdzenie graniczne Moivre'a - Laplace'a
Zmienna o rozkładzie Bernoullego, przy dostatecznie dużej próbie ($n>30$) upodabnia się do zmiennej o rozkładzie normalnym.
Wtedy 
$$
m = np
$$
$$
\sigma = \sqrt{ npq }
$$
$$
X \sim  N(m, \sigma)
$$
# Centralne twierdzenie graniczne Lindeberga-Levy'ego
## Treść twierdzenia
Jeżeli $X_{k}, k \in \mathbb{N}$ jest ciągiem niezależnych zmiennych losowych o identycznych rozkładach jak zmienna losowa $X$ to ciąg dystrybuanty $F_{n}(t)$ o zmiennych losowych $T_{n}$ jest zbieżny do dystrybuanty $\phi(t)$ rozkładu normalnego standardowego.
## O co chodzi
Zbiór $Z_{n}$ $n$ niezależnych zmiennych losowych o tym samy rozkładzie, zbiega do rozkładu normalnego. $n$ musi być duże.
$X_{k}, k \in \mathbb{N}$ niezależne zmienne losowe

Ponieważ mają ten sam rozkład:
$$
m = E(Z_{n}) = n E(X)
$$
$$
V(Z_{n}) = nV(X)
$$
$$
\sigma = D(Z_{n}) = \sqrt{ n }D(X)
$$

$$
Z_{n} \sim N(m, \sigma)
$$
> [!WARNING] Uważaj na $D(Z_n)$
> Pomimo tego, że w przypadku wariancji oraz oczekiwanej wartości jest to wszystko pomnożone przez n. pamiętaj o tym, że zawsze odchylenie standardowe jest pierwiastkiem wariancji
## Prawdopodobieństwo osiągnięcia danej średniej
$$
Y_{n} = \frac{Z_{n}}{n}
$$
$$
m = E(Y_{n}) = E(X)
$$
$$
\sigma = D(Y_{n})= \frac{D(x)}{\sqrt{ n }}
$$
$$
N (m, \sigma)
$$
# Twierdzenie Poissona
Stosujemy je wtedy kiedy jest duża liczba prób ($n > 30$), a szansa na sukces jest niska ^[jak niska?]
$$
\lambda = np
$$
![[Rozkład Poisonna]]

