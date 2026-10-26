---
layout: default
title: Indeksy i zmiana elementów
---

# Indeksy i zmiana elementów

## Cel lekcji

Nauczysz się odczytywać pojedyncze elementy listy i zastępować ich wartości.

## Czego się nauczysz

- Liczyć indeksy od zera.
- Używać zapisu `lista[indeks]`.
- Odczytywać ostatni element przez indeks `-1`.
- Rozpoznawać przyczynę błędu `IndexError`.
- Odróżniać zmianę wartości od dodania elementu.

## Pozycja i wartość to różne rzeczy

Indeks wskazuje miejsce w liście. Wartość jest daną zapisaną w tym miejscu. Pierwszy element ma indeks `0`, drugi `1`, a trzeci `2`.

Dla listy `[10, 20, 30, 40]` wygląda to tak:

| Indeks | 0 | 1 | 2 | 3 |
| --- | --- | --- | --- | --- |
| Wartość | 10 | 20 | 30 | 40 |

`liczby[1]` oznacza wartość z pozycji o indeksie `1`. To drugi element, czyli `20`. Nie szukamy tu liczby o wartości `1`.

## Pierwszy przykład

```python
liczby = [10, 20, 30, 40]
print(liczby[0])
liczby[1] = 25
print(liczby)
```

Wynik:

```text
10
[10, 25, 30, 40]
```

## Omówienie działania programu

1. Tworzymy czteroelementową listę.
2. `liczby[0]` odczytuje pierwszy element. `print()` wypisuje `10`.
3. Po lewej stronie znaku `=` zapis `liczby[1]` wskazuje miejsce, które zmieniamy.
4. Zapisujemy tam `25` zamiast `20`.
5. Liczba elementów nie zmienia się. Nadal są cztery elementy.

| Pozycja | Przed zmianą | Po zmianie |
| --- | --- | --- |
| 0 | 10 | 10 |
| 1 | 20 | 25 |
| 2 | 30 | 30 |
| 3 | 40 | 40 |

## Ostatni element

Ujemny indeks liczy pozycje od końca. `-1` wskazuje ostatni element, a `-2` przedostatni. Nie oznacza to szukania wartości `-1`.

```python
imiona = ["Ala", "Olek", "Maja"]
print(imiona[-1])
print(imiona[len(imiona) - 1])
print(imiona[-2])
```

Wynik:

```text
Maja
Maja
Olek
```

Dwa pierwsze odczyty wskazują ten sam element. `len(imiona)` wynosi `3`, więc ostatni nieujemny indeks wynosi `2`.

Możesz także zmienić ostatnią wartość:

```python
punkty = [6, 8, 3]
punkty[-1] = 9
print(punkty)
print(len(punkty))
```

Wynik:

```text
[6, 8, 9]
3
```

## Granice listy i IndexError

Czteroelementowa lista ma nieujemne indeksy od `0` do `3`. Odczyt `liczby[4]` zakończyłby program błędem `IndexError`. Ta nazwa oznacza próbę użycia indeksu poza zakresem.

Także przypisanie do `liczby[4]` nie doda piątego elementu. Przypisanie przez indeks wymaga istniejącej pozycji. Dodawania nauczysz się w następnej lekcji.

Poniższy program celowo pokazuje błąd. Jest kompletny, ale uruchomienie kończy się wyjątkiem zamiast wynikiem.

```python
liczby = [10, 20, 30, 40]
print(liczby[4])
```

Ostatnia linia komunikatu błędu:

```text
IndexError: list index out of range
```

Dla pustej listy nie istnieje ani indeks `0`, ani `-1`. Przed odczytem elementu listy, która może być pusta, sprawdź jej długość:

```python
oceny = []
if len(oceny) > 0:
    print(oceny[-1])
else:
    print("Brak ocen")
```

Wynik:

```text
Brak ocen
```

## Typowe błędy

- Pierwszy element ma indeks `0`, nie `1`.
- `len(lista)` daje długość, a nie ostatni indeks.
- `lista[0] = 7` zmienia pierwszy element. Nie dopisuje kolejnego.
- Nieistniejący indeks nie daje automatycznie zera. Powoduje błąd.
- Indeks musi być liczbą całkowitą. Napis `"1"` nie jest indeksem `1`.

## Ćwiczenia

### Ćwiczenie 1. Pierwszy i trzeci

Dla listy `liczby = [8, 12, 16, 20]` wypisz pierwszy i trzeci element, każdy w osobnym wierszu.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Przelicz pozycje od zera. Trzeci element nie ma indeksu `3`.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
liczby = [8, 12, 16, 20]
print(liczby[0])
print(liczby[2])
```

Wynik:

```text
8
16
```

</details>

### Ćwiczenie 2. Poprawiona ocena

Utwórz listę `oceny = [3, 2, 5]`. Zastąp drugą ocenę wartością `4`. Wypisz listę i sprawdź jej długość.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Wskazujesz istniejącą pozycję. Nie potrzebujesz nowego miejsca w liście.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
oceny = [3, 2, 5]
oceny[1] = 4
print(oceny)
print(len(oceny))
```

Wynik:

```text
[3, 4, 5]
3
```

</details>

### Ćwiczenie 3. Ostatnie miasto

Z listy `miasta = ["Kraków", "Gdańsk", "Łódź"]` wypisz ostatnią nazwę, używając indeksu ujemnego.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Numerowanie od końca zaczyna się od `-1`.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
miasta = ["Kraków", "Gdańsk", "Łódź"]
print(miasta[-1])
```

Wynik:

```text
Łódź
```

</details>

### Ćwiczenie 4. Ostatni pomiar

Utwórz niepustą listę `pomiary = [11, 14, 18, 16, 12]`. Oblicz ostatni nieujemny indeks i wypisz element z tej pozycji.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Najpierw oblicz numer ostatniej pozycji z długości. Potem użyj go w nawiasach kwadratowych.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
pomiary = [11, 14, 18, 16, 12]
ostatniIndeks = len(pomiary) - 1
print(pomiary[ostatniIndeks])
```

Wynik:

```text
12
```

</details>

### Ćwiczenie 5. Brak pomiarów

Utwórz pustą listę `pomiary`. Jeśli ma elementy, wypisz pierwszy. W przeciwnym razie wypisz `Brak pomiarów`. Program nie może kończyć się błędem.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Odczyt powinien nastąpić dopiero w gałęzi, w której wiadomo, że lista nie jest pusta.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
pomiary = []
if len(pomiary) > 0:
    print(pomiary[0])
else:
    print("Brak pomiarów")
```

Wynik:

```text
Brak pomiarów
```

</details>

## Podsumowanie

Indeks wybiera pozycję, a nie szukaną wartość. Przypisanie przez indeks zmienia istniejący element. Dla listy niepustej `-1` wskazuje ostatni element. Nieistniejąca pozycja powoduje `IndexError`.
