#AnalizaMatematyczna #Pochodne #SymboleNieoznaczone #SymboleOznaczone
# Symbol oznaczony
*Symbol oznaczony* jest wtedy kiedy mimo tego, że występuje np. zero w mianowniku, możemy łatwo ustalić wartość granicy  np. ($\left[ \frac{1}{0} \right]$). 
Symbole są dość intuicyjne, więc nie ma sensu ich tutaj wypisywać.
>[!WARNING] UWAŻAJ NA ZNAK
> W przypadku symboli oznaczonych koniecznie trzeba uważać na znak każdej jego części. $\left[ \frac{1}{0} \right]$, to czy $0$ jest $0^+$ lub $0^-$ wpłynie na ostateczny znak. Tak samo wpłynie znak przed 1.
## Przykład
$$
\lim_{ x \to 0^+ } \frac{1}{x} = \left[ \frac{1}{0} \right] = +\infty 
$$
# Symbol nieoznaczony
*Symbol nieoznaczony* jest wtedy, kiedy podczas obliczania granicy otrzymujemy wyrażenie, którego wartości nie znamy (np. dzielenie zera przez zero). Wtedy stosujemy odpowiednią regułę do sprowadzenia wyrażenia do postaci, z której jesteśmy w stanie wyliczyć odpowiednią wartość granicy.

Wyróżniamy następujące symbole nieoznaczone
$$
\begin{matrix}
\left[ \frac{0}{0} \right] & \left[ \frac{\infty}{\infty} \right] & [0*\infty] & [\infty^0] & [0^0] & [1^\infty] 
\end{matrix}
$$
## Przykład
$$
\lim_{ x \to \infty } \frac{x}{x} = \left[ \frac{\infty}{\infty} \right] 
$$
Otrzymaliśmy właśnie symbol nieoznaczony, w tym przypadku łatwo możemy rozwiązać ten problem. Dla trudniejszych symboli nieoznaczonych można zastosować [[#Metoda de L'Hospitala|metodę de L'Hospitala]].
$$
\lim_{ x \to \infty } \frac{\cancel x}{ \cancel x} = \lim_{ x \to \infty } \frac{1}{1} = 1
$$
## Metoda de L'Hospitala
Regułę tą stosuje się do obliczania granic wyrażeń nieoznaczonych.
