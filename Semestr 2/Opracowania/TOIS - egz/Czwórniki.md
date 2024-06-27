# Posiadamy 6 powszechnie używanych równań
Ogólnie to najpierw wyliczamy układ z praw kichoffa no i wsadzamy to do jakieś macierzy z tych
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
# Podział czwórników
## Pasywne
Nie zawierają źródeł, są same elementy RLC.
## Aktywne
Mogę mieć źródło sterowane.