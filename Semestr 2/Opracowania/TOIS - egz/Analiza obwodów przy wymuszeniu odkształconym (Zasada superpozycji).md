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


> [!WARNING] Składowe 3-rzędu w obwodach trójfazowych
> W obwodach 3 fazowych harmoniczne 3 rzędu (nie podzielne przez 2) sumują się w przewodzie 0.
> Można wtedy pominąć inne harmoniczne parzyste.
> 
> I ogólnie to chyba jeszcze powodują, że nie ma przesunięcia między fazami (ale może to tylko dla 3)


> 
