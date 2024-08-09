To obwody zawierające:
- 3 źródła napięcia (**generator**) sinusoidalnych o jednakowej częstotliwości. Generator może być gwiazdą lub trójkątem. 
- dalsza część obwodu zawiera elementy pasywne (**linia zasilania**) , jest połączeniem między **generatorem** a **odbiornikiem**.
- 3 elementy pasywne (**odbiornik**). Odbiornik może być gwiazdą lub trójkątem

> [!IMPORTANT] Generator 3 fazowy jest układem symetrycznym napięć.
> Wszystkie fazy generatora:
> 1. Wszystkie amplitudy ($E_{M}$) są identyczne
> 2. Częstotliwość identyczna ($\omega$)
> 3. Przesunięcie fazowe $\varphi = \pm 120 \degree$ w stosunku do początkowego
> $e_{A} = E_{M} \sin(\omega t + \psi)$
> $e_{B} = E_{M} \sin(\omega t + \psi - 120 \degree)$
> $e_{C} = E_{M} \sin (\omega t + \psi + 120 \degree)$


# Napięcie fazowe
Jest to wartość $E_{A}$
# Układ napięć miedzy międzyfazowych
Jest to różnica napięć pomiędzy fazami. Napięcie międzyfazowe $E_{AB}$ występujące pomiędzy fazą A i fazą B wyraża się w następujący sposób:
$$
E_{AB} = E_{A} - E_{B}
$$
# Symetryczność
**Generator jest symetryczny**, gdy:
$$
E_{B} = E_{A}^{-j120}
$$
$$
E_{C} = E_{A}^{j120}
$$
**Linia zasilania jest symetryczna**, gdy:

**Odbiornik jest symetryczny**, gdy nie ma zwarcia w przewodzie zerowym.

**Układ jest symetryczny**, gdy wszystkie powyższe elementy są symetryczne. Czyli wtedy kiedy wszystkie napięcia mają równą wartość skuteczną oraz ich przesunięcie fazowe to wielokrotność $\pm 120 \degree$

# Obwód 4-przewodowy
Obwód taki może być 4-przewodowy. W takim przypadku istnieje dodatkowe połączenie mogące zawierać element pasywny, ale nie źródło napięcia. Połączenie to nazywa się **połączeniem zerowym** 

## Wzór na napięcie V punkcie N
$$
V_{N} = \frac{E_{A}Y_{A} +E_{B}Y_{B} + E_{C}Y_{c}}{Y_{A} + Y_{B} + Y_{C}}
$$
## Napięcie niezrównoważone
Napięcie na połączeniu zerowym nazywa się **napięciem niezrównoważenia** ($U_{N}$)
Napięcie niezrównoważone jest = 0 w przypadku gdy:
- Odbiornik jest symetryczny
- 
## Moc
Moc wytworzona na przewodzie zerowym jest mocą strat.

# Stosunek napięcia liniowego do fazowego
![[Obwody trójfazowe 2024-08-07 20.50.23.excalidraw|70%]]

$$
|E_{l}| = \sqrt{ 3 }|E_{f}|
$$
# Stosunek prądu liniowego do fazowego
Praktycznie to samo co z napięciem.

$$
|I_{l}|=\sqrt{ 3 }|I_{f}|

$$

# Pomiar mocy (4 przewody)
Po prostu zsumuj moce.

# Składowe symetryczne
![[Pasted image 20240618212712.png]]
Mamy 3 składowe symetryczne
$E_{0}$ - składowa zerowa
$E_{1}$ - składowa zgodna
$E_{2}$ - składowa przeciwna

Używany jest tutaj operator obrotu $a = e^{j120}$

$$
\begin{bmatrix}
E_{A} \\
E_{B} \\
E_{C}
\end{bmatrix} = \begin{bmatrix}
1 & 1 & 1 \\
1 & a^2 & a \\
1 & a & a^2
\end{bmatrix}
\begin{bmatrix}
E_{0} \\
E_{1} \\
E_{2}
\end{bmatrix}
$$
W celu obliczenia Składowych:
$$
\begin{bmatrix}
E_{0} \\
E_{1} \\
E_{2} \\
\end{bmatrix}
= \frac{1}{ 3}
\begin{bmatrix}
1 & 1 & 1 \\
1 & a & a^2 \\
1 & a^2 & a
\end{bmatrix}
\begin{bmatrix}
E_{A} \\
E_{B} \\
E_{C}
\end{bmatrix}
$$
To jakie wartości przyjmują składowe symetryczne świadczą 

$E_{0} = 0$, $E_{2} = 0$ - układ symetryczny zgodny
$E_{0} = 0, E_{1} = 0$ - układ symetryczny przeciwny
$E_{1} \neq 0, E_{2} \neq 0$ - układ asymetryczny.