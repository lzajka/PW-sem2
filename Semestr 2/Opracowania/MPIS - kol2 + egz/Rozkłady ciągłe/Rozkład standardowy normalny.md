Jest on praktycznie podtypem rozkładu normalnego [[Rozkład normalny]].

Zmienna losowa $Y = N(0,1)$ ma rozkład **standardowy normalny** jeśli $m=0$ i $\sigma = 0$
funkcja gęstości wtedy ma postać:

$$
f(x) = \frac{1}{\sqrt{ 2 \pi}}e^{- {x^2 \over 2}}
$$
![[Pasted image 20240605165516.png]]
# Parametry

**Dystrybuanta** - oznaczamy symbolem ($\Phi$). wartości dystrybuanty podane są w tabeli.
**Wartość oczekiwana ($E(X)$)** - jest zawsze równa 0
**Odchylenie standardowe $(D(X))$** - jest zawsze równe 1
# Własności
$\Phi(-x_{0}) = 1 - \Phi(x_{0})$
$P(a \leq U \leq b) = P(a < u < b) = \Phi(b) - \Phi(a)$
## Reguła sigma
Reguły te określają prawdopodobieństwo wartości będących w odległości $n$-krotności $\sigma$


| krotność | Prawdopodobieństwo |
| -------- | ------------------ |
| 1        | 68.26%             |
| 2        | 95.4%              |
| 3        | 99.7%              |
## Integralne Twierdzenie graniczne Moivre'a - Laplace'a
$X_{n}$ - zbiór zmiennych losowych o rozkładzie z parametrami $n \text{ i } p  \in (0,1)$
Podobnie jak w przypadku [[Rozkład Bernoullego]] $D(X) = np$
$U =  \frac{X_{n} - np }{\sigma}$

Wtedy piszemy $X_{n} \sim N(np, \sqrt{ npq }), n> 30$

TLDR: Można przekształcić [[Rozkład Bernoullego]] do rozkładu standardowego normalnego
# Standaryzacja 
Zmienną losową X o rozkładzie [[Rozkład normalny]] można przekształcić do zmiennej o rozkładzie standardowym normalnym. W tym celu przekształca się zmienną losową $X$ do zmiennej losowej $U$
$$
U = \frac{X - m}{\sigma}
$$

# Obszary krytyczne
## Obszar krytyczny obustronny
$\alpha \in (0, 1)$
$\alpha$ - współczynnik istotności
$1 - \alpha$ - spółczynnik ufności
$u_{\alpha} = 1 - \phi^{-1}\left( 1- \frac{\alpha}{2} \right)$ 


#TODO
