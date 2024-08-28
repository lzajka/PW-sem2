#TOIS #Czwórniki
Czwórniki to elementy czterozaciskowe posiadające 2 pary zacisków: wejście i wyjście.
![[Pasted image 20240828004804.png]]
# Definicja czwórnika
Jeżeli wszystkie elementy czwórnika są liniowe to **czwórnik jest liniowy**, w przeciwnym razie **czwórnik jest nieliniowy**.

Jeżeli czwórnik nie wytwarza energii, a jedynie ją pobiera oraz przetwarza w określony sposób to **czwórnik jest pasywny**. Taki czwórnik może gromadzić, rozpraszać i oddawać energię pobraną ze źródła. Jednak nie jest w stanie oddać więcej niż pobrano.
Czwórnik niebędący pasywnym jest czwórnikiem **aktywnym**, albo też **generatorem energii**.
W czwórnikach możemy chcieć obliczyć np. **transmitancję operatorową**. W tym przypadku przechodzimy na model operatorowy, ale bez normalnie dodawanych wymuszeń. ^2c8cb3

W przypadku czwórników konieczne jest spełnienie warunku równości prądów: $I_{1} = I_{1}'$, $I_{2} = I_{2}'$.

# Transmitancja
Transmitancja jest stosunkiem wyjścia do wejścia. Dotyczy między innymi prądu oraz napięcia. 
Jeżeli transmitancja napięciowa/prądowa jest
- $< 1$: czwórnik osłabia napięcie/prąd.
- $=1$: wyjście i wejście są takie same
- $> 1$: czwórnik wzmacnia napięcie/prąd.

Są 4 rodzaje transmitancji:
- Transmitancja napięciowa $H(s) = \frac{U_{wy}(s)}{U_{we}(s)}|_{I_{wy} = 0}$
  ![[Czwórniki 2024-08-28 16.19.10.excalidraw|size=30%]]
- Transmitancja prądowa $H(s) = \frac{I_{wy}(s)}{I_{we}(s)} \vert_{U_{wy}} = 0$
  ![[Czwórniki 2024-08-28 16.26.07.excalidraw|size=30%]]
- Transmitancja napięciowo-prądowa $H(s) = \frac{U_{wy}(s)}{I_{we}(s)} |_{I_{wy} = 0}$
  ![[Czwórniki 2024-08-28 16.31.20.excalidraw|size=30%]]
- Transmitancja prądowo-napięciowa
> [!TIP] Warto zauważyć że rodzaj po | jest zawsze inny niż w liczniku, oraz że zawsze jest to wyjście.
# Impedancja wejściowa
Transmitancje operatorowe można odnieść do impedancji wejściowej. 
$$
Z_{we}(s) = \frac{U_{we}(s)}{I_{we}(s)} = \frac{A_{11}Z_{0} + A_{12}}{A_{21}Z_{0} + A_{22}}
$$
W przeciwieństwie do transmitancji impedancja wejściowa liczona jest tylko na zaciskach wejściowych.

# Odpowiedzi
Posiadamy 2 rodzaje odpowiedzi:
- Odpowiedź impulsową: $h(t) = \alpha^{-1}[H(s)]$
- Odpowiedź skokową: $g(t) = \alpha^{-1}\left[ H(s)* \frac{1}{s} \right]$
# Posiadamy 6 powszechnie używanych równań
Czwórnik można scharakteryzować za pomocą dwóch równań liniowych. Równania te wiążą ze sobą 2 wartości napięciowe i prądowe.c 
## Impedancyjne
$$
\begin{bmatrix}
U_{1} \\
U_{2}
\end{bmatrix}
= \begin{bmatrix}
Z_{11} & Z_{12} \\
Z_{21} & Z_{22}
\end{bmatrix}
\begin{bmatrix}
I_{1} \\
I_{2}
\end{bmatrix}
$$
## Admitancyjne
$$
\begin{bmatrix}
I_{1} \\
I_{2}
\end{bmatrix} =
\begin{bmatrix}
Y_{11} & Y_{12} \\
Y_{21} & Y_{22}
\end{bmatrix}
\begin{bmatrix}
U_{1} \\
U_{2}
\end{bmatrix}
$$

## Hybrydowe
Tutaj praktycznie góra macierzy to macierz impedancja, a dół admiracyjna
$$
\begin{bmatrix}
U_{1} \\
I_{2}
\end{bmatrix} = 
\begin{bmatrix}
H_{11} & H_{12} \\
H_{21} & H_{22}
\end{bmatrix}
\begin{bmatrix}
I_{1} \\
U_{2}
\end{bmatrix}
$$
## Hybrydowe odwrotne
$$
\begin{bmatrix}
I_{1} \\
U_{2}
\end{bmatrix} = 
\begin{bmatrix}
G_{11} & G_{12} \\
G_{21} & G_{22}
\end{bmatrix}
\begin{bmatrix}
U_{1} \\
I_{2}
\end{bmatrix}
$$
## Łańcuchowe
$$
\begin{bmatrix}
U_{1} \\
I_{1}
\end{bmatrix} =
\begin{bmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22}
\end{bmatrix}
\begin{bmatrix}
U_{2} \\
-I_{2}
\end{bmatrix}

$$
## Łańcuchowe odwrotne
$$
\begin{bmatrix}
U_{2} \\
I_{2}
\end{bmatrix} =
\begin{bmatrix}
B_{11} & B_{12} \\
B_{21} & B_{22}
\end{bmatrix}
\begin{bmatrix}
U_{1} \\
-I_{1}
\end{bmatrix}
$$
# Transmitancje operatorowe
## Napięciowa
$$
H(s) = \frac{U_{2}(s)}{U_{1}(s)} | _{U_{2} = 0}
$$
W przypadku macierzy łańcuchowej $H(s)$ można łatwo obliczyć:
$$
H(s)=\frac{1}{A_{11}}
$$
W przypadku macierzy admitancyjnej
$$
H(s) = - \frac{Y_{21}}{Y_{22}}
$$
Ogólnie do wyznaczenia wystaczy podstawić w miejsce $I_{2} = 0$
## Prądowa
$$
H(s)=\frac{I_{2}}{I_{1}} | _{U_{2} = 0}
$$
W przypadku macierzy łańcuchowej $H(s)$ można łatwo obliczyć:
$$
H(s)=-\frac{1}{A_{22}}
$$
W przypadku macierzy admitancyjnej
$$
H(s) =  \frac{Y_{21}}{Y_{11}}
$$
# Połączenia czwórnikowe
## Szeregowe
Tutaj warto impedancją
![[Pasted image 20240626014128.png]]
$$
\mathbb{Z} = Z_{1} + Z_{2}
$$
## Równoległe
Tutaj macierz admitacyjna
![[Pasted image 20240626013224.png]]
$$
\mathbb{Y} = Y_{1} + Y_{2}
$$
## Szeregowo-równoległe
Tutaj warto hybrydowym
![[Pasted image 20240626014024.png]]
$$
\mathbb{H}=H_{1}+H_{2}
$$
## Równoległo-szeregowe
Macierz odwrotna-hybrydowa
![[Pasted image 20240626014336.png]]
$$
\mathbb{G} = G_{1} + G_{2}
$$
## Łańcuchowe
![[Pasted image 20240626014451.png]]
> [!WARNING] UWAGA
> tutaj jest mnożenie, kolejność jest ważna

$$
\mathbb{A} = A_{1}*A_{2}
$$
