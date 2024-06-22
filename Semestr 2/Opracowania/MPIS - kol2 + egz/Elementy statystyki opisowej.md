# Definicje
**Zbiorowość statystyczna (populacja)** - Zbiór dowolnych jednostek objętych badaniem.
**Jednostki statystyczne** - Elementy populacji, posiadają *cechy statystyczne*
**Cechy:**
- **Zmienne**
- **Niemierzalne** - nie da się opisać liczbą (kolor włosów)
- **Mierzalne** - da się wyrazić jako liczbę
**Badania statystyczne:**
- **pełne** - obejmujące wszystkie jednostki
- **niepełne** - obejmujące część jednostek. Są najczęściej próbą losową.
**Próba losowa** - Wybierasz losowo część elementów, i one reprezentują wszystkie jednostki.

# Szereg wyliczający
## Średnia arytmetyczna
Wiadomo co to
## Odchylenie przeciętne
$d=\frac{|x_{1} - \bar{x}|+ \dots}{n}$
## Wariancja
$s^2 = \frac{(x_{1} - \bar{x})^2+ \dots}{n}$
## Odchylenie standardowe
$s = \sqrt{ s^2 }$
# Szereg rozdzielczy punktowy

| $x_{i}$ | $x_{1}$ | $x_{2}$ | ... | $x_{k}$ |
| ------- | ------- | ------- | --- | ------- |
| $n_i$   | $n_{1}$ | $n_{2}$ | ... | $n_k$   |
$k$ - liczba klas (wariantów)
$n_{i}$ - liczebność $i$-tej klasy
$x_{i}$ - wartość 

$\bar{x} = \frac{x_{1} * n_{1} + x_{2} * n_{2} + \dots + x_{k} * n_{k}}{n_{1} + n_{2} + \dots + n_{k}}$

$d = \frac{|x_{1} - \bar{x_{1}} |* n_{1} + |x_{2} - \bar{x_{2}}| * n_{2} + \dots + |x_{k} - \bar{x_{k}}| * n_{k}}{n_{1} + n_{2} + \dots + n_{k}}$

$s^2 = \frac{(x_{1} - \bar{x_{1}} )^2* n_{1} + (x_{2} - \bar{x_{2}})^2 * n_{2} + \dots + (x_{k} - \bar{ x_{k})^2} * n_{k}}{n_{1} + n_{2} + \dots + n_{k}}$

$s = \sqrt{ s^2 }$
# Szereg rozdzielczy przedziałowy
$k$ - liczba przedziałów klasowych

| $x_{0i} - x_{1i}$ | $x_{01} - x_{11}$ | $x_{02}-x_{12}$ | ... | $x_{0k}-x_{1k}$ |
| ----------------- | ----------------- | --------------- | --- | --------------- |
| $n_i$             | $n_{1}$           | $n_{2}$         | ... | $n_k$           |
Praktycznie tak samo jak w [[#Szereg rozdzielczy punktowy]] tylko że zamiast $x$ jest $\overset{\circ}{x} = \frac{x_{0i} + x_{1i}}{2}$ będące środkiem przedziału.

## Wskaźnik struktury w szeregach rozdzielczych
$\omega _i = \frac{n_{i}}{n}$
## Dominanta
Dominantę, czyli wartość która najczęściej występuje można wyliczyć na 2 sposoby:
### Analityczny
$$
D = x_{od} + \frac{{n_{\alpha} + n_{\alpha - 1}}}{(n_{\alpha} - n_{\alpha - 1}) + (n_{\alpha} + n_{\alpha - 1})}*h_{\alpha}
$$
gdzie:
$x_{od}$ - początek przedziału dominanty
$n_{\alpha}$ - liczebność przedziału dominanty
$x_{\alpha - 1}$ - liczebność poprzedniego
$x_{\alpha + 1}$ - liczebność następnego
$h_{\alpha}$ - szerokość przedziału dominanty

Czyli w skrócie: 
1. Patrzysz na tabelkę
2. Patrzysz który przedział dominuje
3. podstawiasz do wzoru

### Graficzny
1. Znajdujesz największy słupek
2. Robisz takiego fajnego X
3. Punkt przecięcia to dominanta
![[Pasted image 20240616211923.png]]