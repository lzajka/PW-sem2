#ObwodyTrójfazowe #TOIS
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

# Stosunek napięcia liniowego (międzyfazowego) do fazowego
![[Obwody trójfazowe 2024-08-07 20.50.23.excalidraw|70%]]

$$
|E_{l}| = \sqrt{ 3 }|E_{f}|
$$
# Stosunek prądu liniowego do fazowego
Praktycznie to samo co z napięciem.

$$
|I_{l}|=\sqrt{ 3 }|I_{f}|

$$

# Układ Arona
Układ pomiarowy do mierzenia mocy czynnej w obwodach 3-fazowy 3-przewodowych.
![[Pasted image 20240811180221.png|700]]
Ogólnie to polega na tym, że:
$$
p(t) = u_{A}i_{A} + u_{B}i_{B} + u_{C}i_{C}
$$
można przekształcić na
$$
p(t) = (u_{A} - u_{C}) i_{A} + (u_{B} - i_{C})b_{C}
$$
> [!WARNING] Układ Arona działa jedynie na obwodach 3-fazowych 3-przewodowych
# Składowe symetryczne

W przypadku niesymetrycznego układu trójfazowego należy zastosować [[Składowe symetryczne|metodę składowych symetrycznych]]