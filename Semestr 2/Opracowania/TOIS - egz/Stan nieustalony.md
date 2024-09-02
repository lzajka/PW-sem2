#TOIS #StanNieustalony
**Stan nieustalony** występuje wtedy kiedy postać odpowiedzi różni się od wymuszenia (np. różni się częstotliwość lub odpowiedź jest wykładnicza, gdy wymuszenie jest sinusoidalne).
**Stan ustalony** występuje wtedy kiedy postać odpowiedzi jest taka sama jak wymuszenia.

Stan nieustalony jest nałożenie się stanu przejściowego (zanikającego z czasem) wraz z stanem ustalonym podczas **komutacji** (przełączenia lub zmiany sygnałów wymuszających). Zakłada się, że **czas komutacji wynosi 0**.

# Prawa komutacji
Suma ładunków nie może się gwałtownie zmieniać bo łamało by to prawo zachowania energii. Prawa komutacji zajmują się właśnie tym problemem w momencie komutacji (przełączenia).
Wyróżniamy prawa komutacji dla cewek i kondensatorów.

## Prawa komutacji dla kondensatorów
Uproszczenie prawa komutacji dla kondensatorów wygląda następująco.
$$
u_{C}(0^-)=u_{C}(0^+)
$$
## Prawa komutacji dla cewek
Uproszczenie prawa komutacji dla cewek wygląda następująco. 
$$
i_{L}(0^-) = i_{L}(0^+)
$$
# Schemat DC
1. Stan początkowy
2. Model operatorowy po przełączeniu
3. Transformacja odwrotna Laplace'a
# Schemat AC
1. Stan początkowy
2. Stan ustalony po przełączeniu
3. Stan przejściowy metodą operatorową po przełączeniu (bez źródeł sinusoidalnych)
4. Transformacja odwrotna laplaca i przejście na dziedzinę czasu
5. Pełne rozwiązanie $i_{l}(t) = i_{lu}(t) + i_{lp}(t)$, podobnie dla napięcia. 
# Schema
![[Pasted image 20240618232257.png]]
1. Zaczynasz w momencie w którym $t = 0$
   ![[Pasted image 20240618232326.png]]
2. Zamykasz klapkę.
   ![[Pasted image 20240618232523.png]]
3. Rozbijamy i jest równanie różniczkowe 🤮
   ![[Pasted image 20240618232740.png]]
   
Inne sposoby rozwiązywania:
- [[Metoda zmiennych stanu]]
- [[Metoda Operatorowa]]