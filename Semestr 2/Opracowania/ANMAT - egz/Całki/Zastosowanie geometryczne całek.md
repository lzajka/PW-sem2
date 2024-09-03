#AnalizaMatematyczna #Całki
Całki można zastosować do obliczenia Pól, powierzchni oraz objętości figur geometrycznych. Podstawowe wzory do których między innymi należy wzór na pole trójkąta można wyprowadzić za pomocą całkowania. 
# Bryła obrotowa
## Objętość
$$
V = \pi \int_{a}^b [f(x)^2] dx
$$
## Pole powierzchni bocznej
$$
S_{b} = 2\pi \int_{a}^b f(x) \sqrt{ 1 + [f'(x)^2] } dx
$$
# Łuk krzywej
## Opis parametryczny
$$
\begin{matrix}
\begin{cases}
x = x(t)  \\
y = y(t)
\end{cases}  &  t \in <a, b>
\end{matrix}
$$
![[Pasted image 20240903161544.png]]
## Długość łuku
$$
L = \int_{a}^b \sqrt{ [x'(t)]^2 + [y'(t)]^2 } dt
$$
## Przykład
$$
y = f(x)
$$
$$
\begin{cases}
 x = t \\
y = f(t)
\end{cases}
$$
$$
L = \int _{a}^b \sqrt{ [t']^2 + [f'(t)]^2 } dt = \int_{a}^b \sqrt{ 1^2 + [f'(t)]^2 } dt
$$