---
layout: default
title: Podstawowe operacje na listach
---

# Podstawowe operacje na listach

## Cel lekcji

Nauczysz się obliczać podsumowania danych. Najpierw prześledzisz prostą pętlę, a potem poznasz krótsze operacje wbudowane.

## Czego się nauczysz

- Sumować i zliczać elementy.
- Znajdować minimum i maksimum.
- Obliczać średnią bez dzielenia przez zero.
- Korzystać z `len()`, `sum()`, `min()`, `max()`, `count()` oraz `in`.
- Sprawdzać, czy lista jest pusta, zanim wykonasz operację wymagającą danych.

## Akumulator i licznik

**Akumulator** przechowuje narastający wynik, na przykład sumę. **Licznik** przechowuje liczbę zdarzeń, na przykład liczbę ocen co najmniej `4`. Obie zmienne mogą zaczynać od zera, ale odpowiadają na różne pytania: „jaka suma?” oraz „ile elementów?”.

## Pierwszy przykład: ręczne sumowanie

```python
oceny = [3, 4, 5]
sumaOcen = 0
for ocena in oceny:
    sumaOcen = sumaOcen + ocena
print(sumaOcen)
```

Wynik:

```text
12
```

## Omówienie działania programu

1. Zmienna `sumaOcen` zaczyna od zera. Jeszcze niczego nie dodaliśmy.
2. Pętla pobiera kolejną ocenę.
3. Do dotychczasowej sumy dodajemy tę ocenę. Wynik zapisujemy ponownie w `sumaOcen`.
4. Po pętli wypisujemy jedną końcową sumę.

| Ocena | Suma przed dodaniem | Suma po dodaniu |
| --- | --- | --- |
| 3 | 0 | 3 |
| 4 | 3 | 7 |
| 5 | 7 | 12 |

Gdybyśmy ustawiali sumę na zero wewnątrz pętli, gubilibyśmy poprzedni wynik.

## Krócej: sum() i len()

`sum(lista)` dodaje wszystkie liczby z listy. `len(lista)` liczy jej elementy. Funkcje nie zmieniają listy.

```python
oceny = [3, 4, 5]
print(sum(oceny))
print(len(oceny))
print(oceny)
```

Wynik:

```text
12
3
[3, 4, 5]
```

Dla pustej listy suma i długość wynoszą zero:

```python
liczby = []
print(sum(liczby))
print(len(liczby))
```

Wynik:

```text
0
0
```

## Zliczanie według warunku

Nie zawsze chcemy dodawać wartości. Czasem pytamy, ile ocen spełnia warunek.

```python
oceny = [2, 5, 4, 5]
liczbaDobrychOcen = 0
for ocena in oceny:
    if ocena >= 4:
        liczbaDobrychOcen = liczbaDobrychOcen + 1
print(liczbaDobrychOcen)
```

Wynik:

```text
3
```

Zwiększamy licznik o `1`, a nie o wartość oceny. Dla dwójki warunek jest fałszywy, więc licznik pozostaje bez zmian.

## Wystąpienia jednej wartości i count()

Najpierw policzymy piątki samodzielnie:

```python
oceny = [2, 5, 4, 5]
liczbaPiatek = 0
for ocena in oceny:
    if ocena == 5:
        liczbaPiatek = liczbaPiatek + 1
print(liczbaPiatek)
```

Wynik:

```text
2
```

Metoda `count(wartość)` wykonuje takie zliczanie dla jednej konkretnej wartości. Gdy jej nie ma, zwraca `0`.

```python
oceny = [2, 5, 4, 5]
print(oceny.count(5))
print(oceny.count(6))
```

Wynik:

```text
2
0
```

`count(5)` nie liczy ocen większych od piątki ani co najmniej równych piątce. Liczy wyłącznie elementy równe `5`.

## Największy i najmniejszy element: najpierw pętla

Dla niepustej listy przyjmujemy pierwszy element jako dotychczasowe minimum i maksimum. Potem porównujemy z nim kolejne wartości. Porównanie pierwszego elementu z nim samym niczego nie psuje.

```python
liczby = [-8, -3, -6]
najmniejszaLiczba = liczby[0]
najwiekszaLiczba = liczby[0]
for liczba in liczby:
    if liczba < najmniejszaLiczba:
        najmniejszaLiczba = liczba
    if liczba > najwiekszaLiczba:
        najwiekszaLiczba = liczba
print(najmniejszaLiczba)
print(najwiekszaLiczba)
```

Wynik:

```text
-8
-3
```

Nie zaczynamy maksimum od zera. Dla samych liczb ujemnych zero mogłoby pozostać wynikiem, mimo że nie występuje w liście.

Teraz te same operacje funkcjami wbudowanymi. `min()` zwraca najmniejszą, a `max()` największą wartość:

```python
liczby = [-8, -3, -6]
print(min(liczby))
print(max(liczby))
```

Wynik:

```text
-8
-3
```

### Dlaczego pusta lista jest problemem?

Dla `[]` nie ma żadnej wartości do wybrania. Nie można uznać zera za minimum ani maksimum. Dlatego `min([])` i `max([])` powodują `ValueError`. Ręczna wersja też wymaga danych: próba odczytania pierwszego elementu pustej listy powoduje `IndexError`.

Przed tymi operacjami sprawdź `len(lista) > 0`. Samo `sum([])` jest dozwolone, ponieważ suma bez dodanych składników wynosi zero.

## Średnia i pusta lista

Średnia to suma podzielona przez liczbę elementów. Znak `/` wykonuje dzielenie. Dla pustej listy długość wynosi zero, więc nie możemy wykonać tego dzielenia.

```python
oceny = [3, 4, 5]
if len(oceny) > 0:
    sredniaOcen = sum(oceny) / len(oceny)
    print(sredniaOcen)
else:
    print("Brak ocen")
```

Wynik:

```text
4.0
```

Wynik dzielenia jest liczbą typu `float`. Wartość `4.0` odpowiada tutaj średniej równej cztery. Dla pustej listy program wypisze komunikat zamiast dzielić przez zero.

## Obecność wartości: najpierw wyszukiwanie, potem in

Możemy zapamiętać, czy trafiliśmy na szukaną liczbę. Zmienna logiczna zaczyna od `False` i staje się `True` po znalezieniu wartości.

```python
liczby = [8, 2, 5]
czyZnaleziono = False
for liczba in liczby:
    if liczba == 2:
        czyZnaleziono = True
print(czyZnaleziono)
```

Wynik:

```text
True
```

Nie ustawiamy tej zmiennej ponownie na `False` po każdym nietrafionym elemencie. Chcemy pamiętać wcześniejsze trafienie.

Operator `in` sprawdza obecność wartości i daje `True` albo `False`. Nie podaje indeksu ani liczby wystąpień.

```python
liczby = [8, 2, 5]
print(2 in liczby)
print(7 in liczby)
```

Wynik:

```text
True
False
```

Możesz użyć takiego sprawdzenia w `if` przed `remove()`, aby nie usuwać wartości, której nie ma.

## Typowe błędy

- Suma ocen i liczba ocen to różne wyniki.
- `count(4)` liczy dokładne wystąpienia czwórki, a nie wszystkie oceny co najmniej równe cztery.
- `in` daje odpowiedź logiczną. Nie zwraca pozycji elementu.
- Średniej nie obliczamy bez sprawdzenia długości.
- `min()` i `max()` wymagają co najmniej jednego elementu.
- Maksimum zaczynające od zera daje błędne wyniki dla niektórych list ujemnych.

## Ćwiczenia

### Ćwiczenie 1. Suma ręcznie

Oblicz sumę elementów `liczby = [4, 1, 7]` pętlą, bez `sum()`. Wypisz wynik.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Akumulator powinien powstać przed pętlą. Do wyniku dodawaj bieżącą wartość.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
liczby = [4, 1, 7]
sumaLiczb = 0
for liczba in liczby:
    sumaLiczb = sumaLiczb + liczba
print(sumaLiczb)
```

Wynik:

```text
12
```

</details>

### Ćwiczenie 2. Ujemne pomiary

Policz wartości mniejsze od zera w `temperatury = [-2, 3, 0, -5, 1]`. Wypisz ich liczbę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Sprawdź znak każdego pomiaru. Trafienie zwiększa licznik o jeden, a nie o wartość temperatury.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
temperatury = [-2, 3, 0, -5, 1]
liczbaUjemnych = 0
for temperatura in temperatury:
    if temperatura < 0:
        liczbaUjemnych = liczbaUjemnych + 1
print(liczbaUjemnych)
```

Wynik:

```text
2
```

</details>

### Ćwiczenie 3. Największa liczba ujemna

Znajdź największą wartość w `liczby = [-7, -2, -9]` pętlą, bez `max()`. Wypisz ją.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Początkowy kandydat powinien naprawdę występować w liście. Zero nie jest dobrym kandydatem dla tych danych.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
liczby = [-7, -2, -9]
najwiekszaLiczba = liczby[0]
for liczba in liczby:
    if liczba > najwiekszaLiczba:
        najwiekszaLiczba = liczba
print(najwiekszaLiczba)
```

Wynik:

```text
-2
```

</details>

### Ćwiczenie 4. Ile czwórek?

Dla `oceny = [4, 2, 4, 5]` wypisz liczbę czwórek przez `count()`. W następnym wierszu wypisz wynik sprawdzenia, czy w liście jest szóstka.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Jedna operacja odpowiada na pytanie „ile?”, a druga na pytanie „czy jest?”.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
oceny = [4, 2, 4, 5]
print(oceny.count(4))
print(6 in oceny)
```

Wynik:

```text
2
False
```

</details>

### Ćwiczenie 5. Średni wynik

Oblicz średnią elementów `wyniki = [2, 4, 6]`. Uwzględnij w programie także możliwość pustej listy. Wtedy wypisz `Brak wyników`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Odczyt długości i sprawdzenie jej wartości muszą poprzedzić dzielenie.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
wyniki = [2, 4, 6]
if len(wyniki) > 0:
    sredniWynik = sum(wyniki) / len(wyniki)
    print(sredniWynik)
else:
    print("Brak wyników")
```

Wynik:

```text
4.0
```

</details>

### Ćwiczenie 6. Bezpieczne podsumowanie

Zacznij od `liczby = []`. Jeśli lista nie jest pusta, wypisz jej minimum i maksimum. W przeciwnym razie wypisz `Brak danych`. Sprawdź też program po wpisaniu do listy liczb `-4`, `0`, `7`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 6</summary>

Obie funkcje wybierają istniejący element. Gdy nie ma elementów, potrzebna jest inna gałąź programu.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 6</summary>

```python
liczby = []
if len(liczby) > 0:
    print(min(liczby))
    print(max(liczby))
else:
    print("Brak danych")
```

Wynik dla pustej listy:

```text
Brak danych
```

Po zmianie danych na `[-4, 0, 7]` program wypisze kolejno `-4` i `7`.

</details>

## Podsumowanie

Pętla pokazuje, jak powstaje wynik. Funkcje wbudowane skracają częste operacje. Dla pustej listy wolno obliczyć sumę i długość, ale nie ma elementu najmniejszego ani największego. Średnia wymaga niezerowej liczby danych.
