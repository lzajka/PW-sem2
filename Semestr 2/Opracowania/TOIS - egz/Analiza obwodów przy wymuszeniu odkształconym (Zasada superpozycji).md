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
> [!WARNING] Dotyczy tylko wartości chwilowych
> Nie wolno stosować wartości zespolonych.


