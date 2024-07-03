Posiadamy 4 rodzaje mocy.
# Moc chwilowa
Jedyna moc będąca funkcją czasu, definiowana jest jako iloczyn prądu chwilowego oraz napięcia chwilowego.
$$
p(t) = u(t)*i(t)
$$
Zakładając, że $u(t) =  U_{m} \sin (\omega t)$ oraz $i(t) = I_{m} \sin(\omega t - \varphi)$. $\varphi$ w tym przypadku jest opóźnieniem prądu w stosunku do napięcia.
Dla wymuszenia sinusoidalnego można zastosować następujące "uproszczenie".
$$
p(t) = |U| |I| (\cos \varphi - \cos(2\omega t - \varphi)) 
$$
Nie znajduje ona większego zastosowania praktycznego, ale jest przydatna do obliczania innych rodzajów mocy.

# Moc czynna
Średnia wartość mocy chwilowej.
$$
P = \frac{1}{T} \int_{t_{0}}^{t_{0} + T} p(t) dt
$$
Uproszczenie wygląda następująco.
$$
P = |U| |I| \cos \varphi
$$
Jednostką moczy czynnej jest **W**at
## Współczynnik mocy
$\cos \varphi$ jest współczynnikiem mocy, określa on charakter obwodu. Dla obwodu RLC jest ona nieujemna.
Dla $\varphi = 0$ osiąga ona maksimum (rezystory idealne), natomiast dla $\varphi = \pm \frac{\pi}{2}$ (cewki i kondensatory idealne) osiąga ona minimum, wynika z tego że nie wytwarza się na **elementach reaktancyjnych**. 
## Pomiar mocy czynnej
![[Elementy pomiarowe]]
# Moc bierna
W Obwodach elektrycznych prądu sinusoidalnego mamy jeszcze trzecią wielkość. 
Jej wzór wygląda następująco
$$
Q = |U| |I| \sin \varphi
$$
Jej jednostką jest **war**
W przeciwieństwie do mocy czynnej, moc bierna jest $0$ w przypadku w którym $\varphi = 0$, osiąga ona maksimum w przypadku w którym jest ona równa $\varphi = + \frac{\pi}{2}$, a minimum (jest wtedy ujemna) w przypadku w którym jest ona równa $\varphi = - \frac{\pi}{2}$.

# Moc pozorna zespolona
Jest ona proporcjonalna do wartości skutecznych prądu i napięcia. Jest ona iloczynem wartości skutecznej zespolonej napięcia oraz wartości skutecznej sprzężonej prądu I.

$$
S = UI^*
$$
albo inaczej:
$$
S = P + jQ
$$
# Bilans mocy
Zasada zachowania energii obowiązuje zawszę. W przypadku obwodów elektrycznych przyjmuje ona postać *prawa bilansu mocy*.

Moc pozorna wytworzona przez wszystkie źródła $S_{g}$ **musi** być równa mocy pozornej wytworzonej na wszystkich odbiornikach $S_{o}$ .
Tutaj przyjmowane jest że kierunki odbiorników i generatorów są przeciwne.
W przypadku w którym są one takie same otrzymujemy
$S_{o} + S_{g} = 0$
