---
layout: default
title: Zadania - cyfry i konwersje
---

# Zadania - cyfry i konwersje

Każde zadanie wykonaj jako osobny program lub osobne obliczenie ręczne, zgodnie z treścią. Możesz używać zmiennych, napisów, list, warunków i pętli. Stosuj polskie nazwy zmiennych w konwencji camelCase.

W programach konwersji zastosuj poznane algorytmy. Nie zastępuj ich przez `bin()`, `format()` ani `int(zapis, podstawa)`. Nie używaj funkcji własnych, klas, rekurencji ani bibliotek.

Przy odczycie liczby całkowitej zakładamy poprawny zapis liczbowy. Tam, gdzie zadanie wymaga kontroli napisu cyfr, odrzuć także pusty wiersz, spacje, znak minus i niedozwolone cyfry. Błąd danych oznacza komunikat `Błąd danych`, bez wypisywania częściowego wyniku.

## A. Zadania podstawowe - 8

### Zadanie 1. Ostatnia cyfra

Bez zamiany liczby na napis wypisz ostatnią cyfrę liczby `5006`. Oczekiwany wynik: `6`.

### Zadanie 2. Cyfry od końca

Dla liczby `1234` wypisz cyfry od prawej do lewej, każdą w osobnym wierszu. Nie używaj napisu jako źródła cyfr. Oczekiwane wiersze to `4`, `3`, `2`, `1`.

### Zadanie 3. Naturalna kolejność

Dla liczby `1002` przygotuj i wypisz listę cyfr w naturalnej kolejności. Nie zamieniaj liczby na napis. Oczekiwany wynik: `[1, 0, 0, 2]`.

### Zadanie 4. Suma cyfr liczby

Oblicz sumę cyfr liczby `1203`, korzystając z działań na liczbie całkowitej. Oczekiwany wynik: `6`. Sprawdź również zero, dla którego suma wynosi `0`.

### Zadanie 5. Ile cyfr?

Policz cyfry nieujemnej liczby całkowitej bez zamiany na napis. Dla `7` wynik to `1`, dla `1002` wynik to `4`, a dla `0` wynik to `1`.

### Zadanie 6. Cyfry napisu

Zamień stały napis `"0012"` na listę liczb całkowitych odpowiadających jego cyfrom. Zachowaj obydwa początkowe zera. Oczekiwany wynik: `[0, 0, 1, 2]`.

### Zadanie 7. Konwersja ręczna do systemu dwójkowego

Przelicz ręcznie liczbę `9` dziesiętnie na zapis dwójkowy. Zapisz obliczenia, nie tylko końcowy wynik. Oczekiwany zapis końcowy: `1001`.

### Zadanie 8. Ręczny odczyt zapisu dwójkowego

Oblicz ręcznie wartość dziesiętną zapisu dwójkowego `10110`. Przedstaw obliczenia i wynik. Oczekiwana wartość: `22`.

## B. Zadania średnie - 8

### Zadanie 9. Konwerter dziesiętny na dwójkowy

Wczytaj jedną nieujemną liczbę całkowitą i wypisz jej zapis dwójkowy bez zbędnych zer na początku. Liczbę ujemną odrzuć. Dla `0` wypisz `0`, dla `13` wypisz `1101`, dla `16` wypisz `10000`.

### Zadanie 10. Konwerter dwójkowy na dziesiętny

Wczytaj niepusty napis dwójkowy i wypisz jego wartość dziesiętną. Sprawdź wszystkie cyfry. Dla `1101` wynik to `13`. Dla `102` oraz pustego wiersza wypisz wyłącznie `Błąd danych`.

### Zadanie 11. Kilka konwersji

Przygotuj w programie listę liczb `0`, `1`, `2`, `13`, `16`. Dla każdej liczby wypisz jej zapis dwójkowy w osobnym wierszu. Nie używaj funkcji własnych.

Oczekiwany wynik:

```text
0
1
10
1101
10000
```

### Zadanie 12. Zera i suma cyfr

Wczytaj nieujemną liczbę całkowitą. Bez użycia napisu wypisz liczbę jej cyfr równych zero, a następnie sumę wszystkich cyfr. Dla zera przyjmij jedną cyfrę równą zero. Liczbę ujemną odrzuć.

Dla `1002` oczekiwane są wiersze `2` oraz `3`. Dla `0` oczekiwane są wiersze `1` oraz `0`.

### Zadanie 13. Długość zapisu a wartość

Wczytaj i sprawdź napis dwójkowy. Wypisz liczbę znaków wejścia oraz wartość dziesiętną, każdą w osobnym wierszu. Zachowaj informację o zerach wiodących przy liczeniu znaków.

Dla `00101` oczekiwane są wiersze `5` oraz `5`. Błędny lub pusty zapis odrzuć.

### Zadanie 14. Bez zbędnych zer

Wczytaj i sprawdź napis dwójkowy. Wypisz najkrótszy zapis dwójkowy opisujący tę samą wartość. Nie pozostawiaj zer wiodących, chyba że cała wartość jest zerem.

Dla `000101` oczekiwany wynik to `101`. Dla `0000` wynik to `0`. Błędne dane odrzuć.

### Zadanie 15. Porównanie wartości

Wczytaj dwa napisy dwójkowe, każdy w osobnym wierszu. Porównaj ich wartości liczbowe. Wypisz `Równe`, `Pierwsza większa` albo `Druga większa`. Jeżeli którykolwiek zapis jest niepoprawny, wypisz tylko `Błąd danych`.

Dla `00101` oraz `100` oczekiwany komunikat to `Pierwsza większa`. Dla `010` oraz `10` wynik to `Równe`.

### Zadanie 16. Parzystość wartości

Wczytaj i sprawdź napis dwójkowy. Wypisz jego wartość dziesiętną, a w następnym wierszu `Parzysta` albo `Nieparzysta`. Nie stosuj operatorów bitowych. Zero traktuj jako parzyste.

Dla `1101` oczekiwane są wiersze `13` oraz `Nieparzysta`. Błędne dane odrzuć.

## C. Zadania trudniejsze - 4

### Zadanie 17. Inna podstawa

Wczytaj nieujemną liczbę dziesiętną oraz podstawę docelową od `2` do `10`. Wypisz jej zapis w tej podstawie. Kontroluj znak liczby i zakres podstawy. Zero zawsze ma dawać zapis `0`.

Dla danych `25`, `3` oczekiwany wynik to `221`. Dla `25`, `1` wypisz `Błąd danych`.

### Zadanie 18. Między systemami

Wczytaj podstawę źródłową, podstawę docelową i napis liczby, każdy w osobnym wierszu. Obie podstawy mają należeć do zakresu `2-10`. Wypisz zapis tej samej wartości w systemie docelowym. Zastosuj konwersję przez wartość dziesiętną. Błędne dane odrzuć.

Dla danych `3`, `2`, `221` wynik to `11001`. Dla `2`, `3`, `1011` wynik to `102`. Dla `3`, `2`, `3` wypisz `Błąd danych`.

### Zadanie 19. Różne podstawy, ta sama liczba?

Wczytaj podstawę i zapis pierwszej liczby, potem podstawę i zapis drugiej liczby. Każda podstawa należy do zakresu `2-10`. Sprawdź poprawność obu liczb i porównaj ich wartości. Wypisz `Równe`, `Pierwsza większa` albo `Druga większa`. W przypadku błędu wypisz tylko `Błąd danych`.

Dla podstawy `3` z zapisem `102` oraz podstawy `2` z zapisem `1011` oczekiwany wynik to `Równe`. Zera wiodące nie zmieniają porównywanej wartości.

### Zadanie 20. Zestaw liczb

Wczytaj nieujemną liczbę elementów, a następnie tyle nieujemnych liczb dziesiętnych. Zakładamy, że wszystkie te liczby są poprawnie podane i nieujemne.

Dla każdej liczby wypisz w jednym wierszu jej zapis dwójkowy oraz liczbę jedynek w tym zapisie, rozdzielone spacją. Na końcu wypisz sumę wejściowych wartości dziesiętnych poprzedzoną napisem `Suma:`. Dla liczby elementów równej zero wypisz tylko `Suma: 0`.

Przykładowe wejście:

```text
3
0
13
2
```

Oczekiwany wynik:

```text
0 0
1101 3
10 1
Suma: 15
```
