#AnalizaMatematyczna #Szeregi
Obliczenie sumy szeregu sprowadza się do znalezienia bardzo podobnego szeregu, do rozbicia szeregu i zauważenia usuwania się elementów, oraz do sprowadzenia do ciągu i użycia wzoru maturalnego.
# Sposoby na sprowadzenie
## Rozbicie ułamku
Jeżeli mamy pewien ułamek możemy go rozbić na sumę kilku ułamków.
$$
\sum_{n = 1}^\infty \frac{1}{(2n-1)+(2n+1)} = \sum_{n = 1}^\infty\left( \frac{A}{2n-1} +\frac{B}{2n+1} \right) = \sum_{n = 1}^\infty\left( \frac{1}{4n-2} - \frac{1}{4n+2} \right)
$$
Następnie sumę $n$ elementów można wyliczyć za pomoocą wzoru
$$
S_{n} = \frac{a_{1} +a_{n}}{2}*n
$$
aby wyliczyć sumę nieskończoną szeregu wystarczy zastosować granicę.
# Usuwanie się elementów ciągu
Tak jak np. w powyższym przypadku oba szeregi powinny być rozbieżne. Otrzymalibyśmy coś typu $\infty - \infty$ czego wartość jest nieznana, gdyż nieskończoności mogą być większe lub mniejsze. W tym przykładzie w przypadku rozbicia można zauważyć że niektóre elementy szeregu nawzajem siebie usuwają.

$$
\sum_{n = 1}^\infty\left( \frac{1}{4n-2} - \frac{1}{4n+2} \right) = \left( \frac{1}{2} - \cancel{\frac{1}{6}} \right) + \left( \bcancel{\frac{1}{6}} -  \cancel{\frac{1}{10}}\right) + \left( \bcancel{\frac{1}{10}} -\cancel{\frac{1}{14}} \right) + \dots
$$
I tak dalej w nieskończoność
# Wzory na sumy ciągów
## Ciąg arytmetyczny
$$
S_{n} = \frac{a_{1} + a_{n}}{2}*n
$$
$$
S = \lim_{ n \to \infty } S_{n}
$$
## Geometrycznego
$$
S_{n} = a_{1}* \frac{1-q^n}{1-q}
$$
$$
S = \frac{a_{1}}{1-q}
$$