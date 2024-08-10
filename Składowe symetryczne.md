#ObwodyTrójfazowe #TOIS
Składowe symetryczne pomagają w analizie układów trójfazowych o zasilaniu niesymetrycznym, czyli w takim w którym co najmniej jeden poniższy warunek jest spełniony:
- Przesunięcie kątowe pomiędzy poszczególnymi fazami nie wynosi $\pm 120 \degree$
- Amplitudy nie są takie same.
Przykładowo w przypadku w którym w fazie wystąpi przerwa, to układ jest **niesymetryczny**.

Metoda składowych symetrycznych pozwala na zastąpienie układu 3 wektorów niesymetrycznych sumą 3 zestawów 3 wektorów symetrycznych.
Używany jest tutaj operator obrotu $a = e^{j120}$
![[Pasted image 20240811012804.png]]
Jak widać na powyższym obrazku zarówno moduły składowych, jak i kąty pomiędzy nimi są takie same.

![[Pasted image 20240618212712.png]]
Mamy 3 składowe symetryczne
$E_{0}$ - składowa zerowa
$E_{1}$ - składowa zgodna
$E_{2}$ - składowa przeciwna





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

To samo można zrobić z *prądem*, wystarczy podstawić $I_{x}$ za $E_{x}$.
