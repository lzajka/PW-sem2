# Schemat Bernoullego
$$
P_{n}(k)=\begin{pmatrix}
n\\ k
\end{pmatrix}
p^k q^{n-k}
$$gdzie:
**n** - ilość prób
**k** - ilość sukcesów
**p** - prawdopodobieństwo sukcesu
**q** - prawdopodobieństwo porażki

### Parametry

$E(X) = np$
$V(X) = npq$
$D(X) = \sqrt{ npq }$

# Twierdzenie graniczne Moivre'a-Laplace'a
W przypadku dużych liczb prób ($n>30$) można zastosować [[Rozkład standardowy normalny#Integralne Twierdzenie graniczne Moivre'a - Laplace'a]]

> [!Wikipedia]
> Dobrym pomysłem jest Przejście na rozkład normalny wtedy, gdy $n(p-1) > 5$
> $N(np, \sigma = \sqrt{np(1-p)  } )$
> 

# Do rozkładu Poissona
![[Twierdzenia graniczne#Twierdzenie Poissona]]