# Idea Modelu operatorowego
Obwód się np. nagle zamyka, no i musi jakoś łagodnie przejść.

# Schemat
1. **Wyznaczamy warunki początkowe**
	1. Kondensator -> przerwa, Cewka -> zwarcie
	2. Liczmy prąd na cewcie i napięcie na kondensatorze
2. **Wyznaczamy stan ustalony po przełączeniu**
	1. Miejsce które odcięła klapka jest teraz połączone
	2. To samo co podczas wyznaczania warunków początkowych
3. **Liczymy Składową przejściową**
	1. Stosujemy transformacje Laplace'a
		1. $U_{R}(s)=Ri_{R}(s)$
		2. $U_{L}(s)= sLI_{L}(s) - Li_{L}(0^+)$
		3. $U_{C}(s)= \frac{1}{sC}I_{C}(s) + \frac{U_{C}(0^+)}{s}$
	2. Obliczamy dalsze rzecy.
	3. Stosujemy transformację odwrotną laplaca na tym co liczymy.
4.  Sumujemy składową przejściową + składową ustaloną	
 