#TOIS #TransformacjaLaplacea #StanNieustalony #MetodaResiduów
$$
\DeclareMathOperator*{\res}{res}
$$
Po przejściu i dokonaniu obliczeń na postaci operatorowej elementów obwodów w stanie nieustalonym należy przejść na dziedzinę czasową. Do tego stosuje się **transformację odwrotną Laplace'a**. Istnieją różne metody jej obliczania.

# Metoda Residuów
Jeżeli mamy funkcję wymierną $F(s)$ będącą ilorazem 2 wielomianów.
$$
F(s) = \frac{L(s)}{M(s)}
$$
To pierwiastki licznika nazwane są **zerami**, a mianownika **biegunami**.
Metoda residuów wykorzystuje następujące twierdzenie:

> [!Theorem] Twierdzenie
> Jeżeli stopień wielomianu mianownika jest wyższy niż stopień wielomianu licznika, to oryginał funkcji wygląda następująco:
> $$
> \alpha^{-1} [F(s)] = \sum_{i=1}^n \res_{s=s_{i}} [F(s) e^{st}]
> $$
> gdzie $s_{i}$ to $i$-ty biegun

Dla bieguna $l$-krotnego residuum funkcji wygląda następująco
$$
\res_{s=s_{i}}[F(s) e^{st}] = \frac{1}{(l-1)!} \lim_{ s \to s_{i} } \frac{d ^{(l-1)}}{d s^{l-1}} [F(s) (s-s_{i})^l e^{st}]
$$
W przypadku bieguna $1$ krotnego wzór ten upraszcza się do:
$$
\res_{s = s_{i}} [F(s)e^{st}] = \lim_{ s \to s_{i} } [F(s) (s-s_{i})e^{st}] 
$$