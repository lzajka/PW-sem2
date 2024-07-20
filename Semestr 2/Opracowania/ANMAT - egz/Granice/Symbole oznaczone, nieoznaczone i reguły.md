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
## Metoda de L'Hospitala ($\left[ \frac{0}{0} \right], [\frac{\infty}{\infty}]$)
Regułę tą stosuje się do obliczania granic wyrażeń nieoznaczonych typu $[\frac{0}{0}]$ oraz $[\frac{\infty}{\infty}]$.
Takie wyrażenie dzielimy na 2 funkcje: licznika - $f(x)$, oraz mianownika - $g(x)$.

Następnie, jeżeli:
$$
\begin{flalign*}
\lim_{ x \to \infty } f(x) = 0 && \text{oraz} &&
\lim_{ x \to \infty } g(x) = 0
\end{flalign*}
$$
lub
$$
\begin{flalign*}
\lim_{ x \to \infty } f(x) = \infty &&
\text{oraz} &&
\lim_{ x \to \infty } g(x) = \infty
\end{flalign*}
$$

To, wtedy
$$
\lim_{ x \to a } \frac{f(x)}{g(x)} = \lim_{ x \to a } \frac{f'(x)}{g'(x)}
$$
> [!WARNING] Równość zachodzi dodatkowo pod warunkiem, jeżeli równość po prawej stronie istnieje.

### Uproszczenie i zastosowanie metody de L'Hospitala ($[0 * \infty]$)
Ponieważ $\infty$ to $\frac{1}{0}$ można to zapisać jako $0 * \frac{1}{0}$, czyli $\frac{0}{0}$. Następnie takie równanie można rozwiązać za pomocą *metody de L'Hospitala*

### Uproszczenie i zastosowanie metody de L'Hospitala ($\left[ \infty - \infty \right]$)
W tym przypadku ponieważ nieskończoność to czasami $\frac{a}{0}$ oraz $\frac{b}{0}$ można wziąć równanie do wspólnego mianownika.
Następnie na otrzymanym ułamku zastosować *metodę de L'Hospitala*
