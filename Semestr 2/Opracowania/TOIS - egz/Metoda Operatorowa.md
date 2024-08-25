#TOIS #MetodaOperatorowa #Heavyside #Laplace #StanNieustalony
# Idea Modelu operatorowego
Obwód się np. nagle zamyka, no i musi jakoś łagodnie przejść.

# Schemat
1. **Wyznaczamy warunki początkowe**
	1. W przypadku napięcia sinusoidalnego wystarczy za $t$ podstawić $0$
	2. Kondensator -> przerwa, Cewka -> zwarcie
	3. Liczmy prąd na cewcie i napięcie na kondensatorze
3. **Wyznaczamy stan ustalony po przełączeniu**
	1. Miejsce które odcięła klapka jest teraz połączone
	2. To samo co podczas wyznaczania warunków początkowych
4. **Liczymy Składową przejściową**
	1. Stosujemy transformacje Laplace'a
		1. $U_{R}(s)=Ri_{R}(s)$
		2. $U_{L}(s)= sLI_{L}(s) - Li_{L}(0^+)$ (w przypadku sprzężenia, zachowujemy się jakby była kolejna cewka)
		3. $U_{C}(s)= \frac{1}{sC}I_{C}(s) + \frac{U_{C}(0^+)}{s}$
		4. Podobnie przekształcamy źródła... jeśli są. 
	2. Obliczamy dalsze rzeczy.
	3. Stosujemy [[Transformacja Odwrotna Laplace'a|transformację odwrotną laplace'a]] na tym co liczymy.
5.  Sumujemy składową przejściową + składową ustaloną
 ![[Laplace]]
![[Pasted image 20240618233526.png]]
# Przykład
1. Ułóż równaina kirchoffa
   ![[Pasted image 20240618233549.png]]
2. Różniczki -> Laplace 
   ![[Pasted image 20240618233813.png]]
3. Wiemy że warunki początkowe to $i_{1}(0^-) = 0 = i(0^+)$, to samo dla $i_{2}$
1. Znajdź $I_{1}(s), I_{2}(s), \dots$
2. Przebieg czasowy obliczamy za pomocą [[Transformacja Odwrotna Laplace'a#Metoda Residuów|Metody residuów]] lub korzystając ze [[Wzór Heavyside'a|wzoru Heavyside'a]]