#TOIS #Czwórniki

# Żyrator
Żyrator jest czwórnikiem opisanym następującą macierzą łańcuchową
$$
\begin{bmatrix}
U_{1} \\
I_{1}
\end{bmatrix} =
\begin{bmatrix}
0 & R_z \\
G_{z} & 0
\end{bmatrix}
\begin{bmatrix}
U_{2} \\
-I_{2}
\end{bmatrix}
$$
albo za pomocą równania łańcuchowego
$$
\begin{bmatrix}
I_{1} \\
I_{2}
\end{bmatrix} =
\begin{bmatrix}
0 & G_{z} \\
-G_{z} & 0
\end{bmatrix}
\begin{bmatrix}
U_{1} \\
U_{2}
\end{bmatrix}
$$
Przy czym parametr $G_{z}$ jest nazywany konduktancją żyracji, a $R_{z}$ rezystancją.
![[Zastosowania czwórników 2024-08-28 21.18.00.excalidraw|size=100%]]
Najważniejszą funkcją żyratora jest przetwarzanie impedancji obciążenia w impedancję odwrotnie proporcjonalnej do jej.

$$
Z_{we} = \frac{R_{z}^2}{Z_{0}}
$$
$$
Z_{0} = \frac{R_{z}^2}{Z_{we}}
$$
gdzie $Z_{0}$ to obciążenie czwórnika.


# Konwerter ujemno-impedancyjny (NIC)
Jest to [[Czwórniki#^2c8cb3|czwórnik aktywny]]. Przetwarza on z ujemnym znakiem:
Współczynnik $K$ jest współczynnikiem prądu/napięcia.
## Prąd - NIC z inwersją prądu (INIC)
$$
\begin{bmatrix}
U_{1} \\
I_{1}
\end{bmatrix} = \begin{bmatrix}
1 & 0 \\
0 & -K_{i}
\end{bmatrix} \begin{bmatrix}
U_{2} \\
-I_{2}
\end{bmatrix}
$$
Prąd wyjściowy ma przeciwny znak * K, napięcie nie zmienia wartości.
## Napięcie - NIC z inwersją napięcia (VNIC)
$$
\begin{bmatrix}
U_{1} \\
I_{1} 
\end{bmatrix}
= \begin{bmatrix}
-K_{u} & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
U_{2} \\
-I_{2}
\end{bmatrix}
$$
Prąd wyjściowy nie zmienia wartości, napięcie ma przeciwny znak * K.
# Idealny Wzmacniacz napięciowy 
Opisywany jest macierzą hybrydową.
$$
\begin{bmatrix}
I_{1} \\
U_{2} 
\end{bmatrix}
= \begin{bmatrix}
0 & 0 \\
A & 0
\end{bmatrix}
\begin{bmatrix}
U_{1} \\
I_{2}
\end{bmatrix}
$$
Idealny wzmacniacz napięciowy nie pobiera prądu (praktycznie rozwarcie). Jedyne co robi to przetwarza napięcie w następujący sposób $U_{2} = A U_{1}$
![[Pasted image 20240828215602.png]]

# Idealny Wzmacniacz operacyjny
Jest to szczególny przypadek **wzmacniacza napięciowego**, tak jak każdy z nich nie pobiera prądu.
![[Pasted image 20240828215739.png]]
Gdzie $U_{1} = U^+ - U^-$ co z resztą można wyliczyć z prawa napięciowego Kirchoffa.

$U^+$ - napięcie wejścia nieodwracające.
$U^-$ - napięcie wejścia odwracające.

Przy założeniu idealności wzmacniacza operacyjnego $A \to \infty$. Ponieważ napięcie wyjściowe przyjmuje wartości skończone, to napięcie wejściowe musi mieć wartość równą $0$.

Charakteryzuje się:
- nieskończoną wartością wzmocnienia napięciowego.
- Zerową wartością impedancji wyjściowej. 
- Nieskończoną impedancją obu wejść. (dla nie idealnego to nie jest $\infty$, ale bardzo duża wartość więc tak, czy tak można traktować jako $\infty$)
- Spełnia wszystkie powyższe cechy od $0 \to \infty$