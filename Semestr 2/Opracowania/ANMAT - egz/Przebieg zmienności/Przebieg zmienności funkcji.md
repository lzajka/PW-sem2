#AnalizaMatematyczna #Monotoniczność #Granice #Asymptoty
# Monotoniczność
*Monotoniczność* opisuje nam czy funkcja rośnie, czy maleje. Możemy wyznaczać za pomocą pochodnych. Jeżeli pochodna funkcji $f(x)$ na danym przedziale jest ciągła oraz:
- Ujemna - Funkcja jest malejąca.
- Równa $0$ - Funkcja jest stała.
- Dodatnia - Funkcja jest rosnąca.
# Ekstrema lokalne
*Ekstrema lokalne* są miejsca, w której funkcja przyjmuje największą/najmniejszą wartość na bardzo małym przedziale.

Jeżeli pochodna funkcji w danym punkcie posiada ekstremum lokalne to jej pochodna w tym punkcie jest równa $0$ (warunek konieczny)
> [!WARNING] To nie jest warunek wystarczający.
> To, że pochodna funkcji w danym punkcie jest równa $0$ nie oznacza, że jest ekstremum lokalnym. 
> Przykład: funkcja stała na przedziale - Na przedziale będzie pochodna równa $0$, ale to nie będzie oznaczało że każdy punkt na tym przedziale to ekstremum.

Wyróżniamy 2 typy:
- *Minimum lokalne* - Taki dołek: po lewej stronie funkcja jest malejąca, po prawej rosnąca
- *Maksimum lokalne* - Taka górka: po lewej stronie funkcja jest rosnąca, po prawej malejąca.

# Asymptoty
## Asymptota pionowa
Dla każdego punktu, który nie należy do dziedziny szukamy granicy lewostronnej i prawostronnej.
Jeżeli odpowiednio lewa, prawa, lub obie granice są $\pm \infty$ to granica jest *lewostronna*, *prawostronna*, lub *obustronna*.

> [!NOTE] Obie asymptoty mogą, ale nie muszą mieć takiego samego znaku.

### Przykład
$$f(x) = \frac{1}{x-1}$$
$$
D: x \in \mathbb{R} - \lbrace 1 \rbrace
$$
$$
\lim_{ x \to 1^- } f(x) = -\infty 
$$
$$
\lim_{ x \to 1^+ } f(x) = +\infty 
$$
Ponieważ funkcja dla punktu $1$ posiada zarówno asymptotę prawostronną, i lewostronną jest ona w punkcie $1$ obustronna.

## Asymptota pozioma
Liczymy 2 granice:
$$
\lim_{ x \to \infty } f(x) = a
$$
$$
\lim_{ x \to -\infty } f(x) = a 
$$
ważne, żeby $a \neq \pm\infty$. Asymptota również może być jednostronna lub obustronna.
## Asymptota ukośna
$$
a = \lim_{ x \to \pm\infty } \frac{f(x)}{x}
$$
> [!NOTE] Asymptota pozioma to szczególny przypadek asymptoty ukośnej. $a = 0$

$$
b = \lim_{ x \to \pm\infty } f(x) - ax 
$$
