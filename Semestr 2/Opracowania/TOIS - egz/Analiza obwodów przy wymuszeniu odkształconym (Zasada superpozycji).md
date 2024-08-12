#TOIS
Może zdarzyć się obwód w którym występują źródła o różnej częstotliwości (albo jedno sumujące kilka), wtedy nie ma jednego parametru $\omega$, więc nie da się tak po prostu obliczyć rezystancji zastępczej dla cewek i kondensatorów. 

Aby taki obwód rozwiązać należy rozdzielić obwód na różne częstotliwości.

> [!TIP] Wymuszenie stałe można traktować jak sinusoidalne
> $u(t) = U$
> $u(t) = \sin(0t +90\degree)$
> $\omega = 0$

# Schemat
1. Dzielimy obwód na różne częstotliwości ($\omega$) 
	1. Zwieramy źródła napięciowe o innym $\omega$
	2. Rozwieramy źródła prądowe o innym $\omega$
	3. Obliczamy rezystancje zastępcze elementów dla danego $\omega$
2. Liczymy prąd/napięcia **chwilowe** ( $i^{(\omega)}(t)$ lub $u^{(\omega)}(t)$ ) dla interesujących nas elementów dla każdej częstotliwości.
3. Ostateczny prąd lub napięcie gałęziowe to suma prądów/napięć **wielkości czasowych** dla każdego $\omega$
4. Wartości odczytane na na przyrządach są to pierwiastki sum modułów różnych częstotliwości $|I_{A}| = \sqrt{ |I_{A}^{(1)}|^2 +|I_{A}^{(2)}|^2 +|I_{A}^{(3)}|^2}$

# Schemat - Obwód 3 fazowy
Stosujemy tutaj metodę harmonicznych.

$e_{A}(t) = 2\sin(w_{1}t) + \sin(3w_{1}t)$

wielokrotność $\omega_{1}$ to tutaj $n$-ta harmoniczna.
> [!WARNING]
> Dla $n$-tej harmonicznej mnożymy również przesunięcie przez $n$
> Z tego powodu w przewodzie zerowym może pojawić się prąd dla harmonicznych 3 rzędu.

