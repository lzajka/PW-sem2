Metoda ta umożliwi na obliczenie w szybki sposób napięć pomiędzy węzłami, a uziemieniem.

# Schemat
1. Wyznacz węzły
2. Wybierz uziemienie. Tym więcej gałęzi tym lepiej.
3. Przekształć wszystkie źródła napięcia na źródła prądowe
4. Dla każdego węzła $i$ pomnóż konduktancję wszystkich gałęzi przez $V_{i}$ odejmij to samo innych węzłów, przyrównaj do prądów *wchodzących - wychodzących* : $V_{i}\left( \frac{1}{R_{1}} + \frac{1}{R_{2}} + \dots \right) - V_{2}(\dots)= J_{1} + \frac{E}{R}$ ^krok4
5. Napięcie na gałęzi to będzie różnica między poszczególnymi napięciami węzłów.
# Metodą wyznaczników
1. dojdź do: [[#^krok4]]
2. Zapisz w postaci działań na macierzach $\mathbb{G}, \mathbb{V}, \mathbb{I_{w}}$ 
3. Macierz $\mathbb{G_{i}}$ to macierz w których $i$-ta kolumna zastąpiona jest przez $\mathbb{I_{w}}$
4. Oblicz wyznaczniki macierzy $\mathbb{G}$ i $\mathbb{G_{i}}$
5. $V_{i} = \frac{\det(\mathbb{G_{i}})}{\det(\mathbb{G})}$
6. 