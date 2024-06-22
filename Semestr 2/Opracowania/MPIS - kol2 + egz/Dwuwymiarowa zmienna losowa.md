To para dwóch zmiennych losowych $X$ i $Y$ ułożonych w tabelę


| $x_{i} \setminus y_{i}$ | $y_1$         | $y_2$         | ... | $y_l$         | \|  | $p_{i\circ}$ |
| ----------------------- | ------------- | ------------- | --- | ------------- | --- | ------------ |
| $x_1$                   | $p_{11}$      | $p_{12}$      | ... | $p_{1l}$      | \|  | $p_{1\circ}$ |
| $x_2$                   | $p_{21}$      | $p_{22}$      | ... | $p_{2l}$      | \|  | $p_{2\circ}$ |
| ...                     | ...           | ...           | ... | ...           | \|  | ...          |
| $x_k$                   | $p_{k1}$      | $p_{k2}$      | ... | $p_{kl}$      | \|  | $p_{k\circ}$ |
| -                       | -             | -             | -   | -             |     | -            |
| $p_{\circ j}$           | $p_{\circ j}$ | $p_{\circ j}$ | ... | $p_{\circ j}$ | \|  | 1            |
$p_{i\circ}$ , $p_{\circ j}$- gdzie $j$ jest zastępowane dowolną liczbą tworzą rozkład brzegowy.

# Kowariancja
$cov(X,Y) = E(X * Y) - EX*EY$
$E(X * Y) = \sum_{ij}x_{i}y_{j}p_{ij}$

## Własności
$-D(X)D(Y) \leq cov(X, Y) \leq D(X) D(Y)$
$|cov(X, Y)| \leq D(X,Y)$
$| \frac{cov(X, Y)}{D(X)D(Y)}| \leq 1$
## Współczynnik korelacji
$\varphi = \frac{cov(X, Y)}{D(X)D(Y)}$

### Interpretacja
$\varphi = 1$ Silnie skorelowane dodatnio (gdy X rośnie, Y rośnie)
$\varphi = -1$ Silnie skorelowane ujemnie (gdy X rośnie, Y maleje)
$\varphi = 0$ nieskolerowane
