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
# Schemat
1. Warunki początkowe (zwarte cewki, rozwarte kondensatory)
2. Stan ustalony po przełączeniu (zwarte cewki, rozwarte kondensatory)
3. warunki początkowe dla składowej przejściowej
4. Obliczenie składowej przejściowej (system operatorowy -> transformata laplace -> składowa przejściowa)
5
# Schemat
![[Pasted image 20240618232257.png]]
1. Zaczynasz w momencie w którym $\omega = 0$ i $t = 0$
   ![[Pasted image 20240618232326.png]]
2. Teraz to zamyksz tą klapkę i liczy, w tym przypadku jest zwarcie no i prąd omija rezystor
   ![[Pasted image 20240618232523.png]]
3. Rozbijamy i jest równanie różniczkowe 🤮
   ![[Pasted image 20240618232740.png]]

> [!NOTE] Możliwe, że w składowej nieustalonej źródła jednak zachowują się specyficznie.
> Źródła prądowe -> rozwarcie.
> Źródła napięciowe -> zwarcie.



# Zapis układu w postaci macierzowej

$$
\begin{rcases}
R i_{Lp} + L \frac{di_{cp}}{dt} + u_{cp} = 0 \\
i_{Lp} = i_{c} = C \frac{d u_{cp}}{d t}  
\end{rcases} 
\to
\begin{matrix*}[l]
\frac{d i_{cp}}{d t} = \frac{1}{L}[-Ri_{cp} - u_{cp}] \\
\frac{d u_{cp}}{d t} = \frac{1}{C} i_{Lp} 
\end{matrix*}
\to
\underbrace{\begin{bmatrix}
\frac{d i_{Cp}}{d t} \\
\frac{d U_{cp}}{d t}  
\end{bmatrix}}_{\mathbb{x}_{p}(t)}
=
\underbrace{\begin{matrix*}[|c|c|]
 \hline
 -\frac{R}{L} & -\frac{1}{L} \\ \hline
\frac{1}{C} & 0 \\ \hline
 
\end{matrix*}}_{\mathbb{A}}
\underbrace{\begin{bmatrix}
i_{Lp} \\
u_{Cp}
\end{bmatrix}}_{\mathbb{x}_{p}(0)}
$$