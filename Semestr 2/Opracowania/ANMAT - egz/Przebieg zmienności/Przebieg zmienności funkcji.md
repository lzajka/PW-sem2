#AnalizaMatematyczna #Monotoniczność #Granice #Asymptoty #Pochodne #Funkcje 
# Kolejność badania
1. Dziedziny i granice\
2. [[#Asymptoty]]
3. [[#Monotoniczność]]
4. Minima i ekstrema
5. [[#Przedziały wklęsłości i wypukłości|Wklęsłość, wypukłość oraz punkty przegięcia]]
6. [[#Tabelka]]
7. Wykres
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

# Przedziały wklęsłości i wypukłości
## Przedział wypukły
*Przedział wypukły* ($f''(x) > 0$) przypomina uśmiechniętą buźkę.
![[Pasted image 20240726230452.png]]
## Przedział wklęsły
*Przedział wklęsłości* ($f''(x) < 0$) przypomina smutną buźkę.
![[Pasted image 20240726230613.png]]
## Punkty przegięcia
*Punkt przegięcia* ($f''(x) = 0$)
![[Pasted image 20240726231450.png]]
>[!WARNING] Punkt przegięcia może wystąpić jeżeli pochodna 2 stopnia nie istnieje.
# Tabelka
Na podstawie informacji o znaku pochodnych 1 i 2 stopnia dla określonych przedziałów określa czy funkcja jest 