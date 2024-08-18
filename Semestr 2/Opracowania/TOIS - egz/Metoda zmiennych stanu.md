#StanNieustalony #TOIS 
# Równanie stanu w postaci normalnej

Równania stanu pozwalają na opisanie w wygodny sposób obwodów RLC w stanie nieustalonym.
$$
\dot{x} = A*x +B*u
$$
Gdzie:
- $x$ - zmienne stanu (prądy cewek / napięcia kondensatorów).
- $\dot{x}$ - pochodna zmiennych stanu po czasie.
- $\mathbb{A}$ - Macierz stanu (Przez co mnożony jest prąd/napięcie na kondensatorach/cewkach)
- $\mathbb{B}$ - Macierz wejść (Przez co mnożone są wymuszenia)
- $u$ - wektor wyjściowy (Wymuszenia)

# Równania wyjścia
Opisywane są w formie:
$$
y = C*x + D*u
$$
Gdzie:
- $y$ - wektor wyjściowy (wartości które szukamy)
- $C$ - macierz wyjść
- $D$ - macierz bezpośredniego przejścia 

# Przykład
![[Pasted image 20240818160511.png]]