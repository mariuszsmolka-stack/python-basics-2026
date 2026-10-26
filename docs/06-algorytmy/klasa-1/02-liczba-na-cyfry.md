---
layout: default
title: Wyodrębnianie cyfr z liczby
---

# Wyodrębnianie cyfr z liczby

## Cel lekcji

Rozłożysz nieujemną liczbę całkowitą na cyfry bez zamieniania jej na napis. Zrozumiesz działanie `% 10`, `// 10` i pętli `while`.

## Problem po ludzku

Liczba `1234` jest jedną wartością. Chcemy otrzymać jej cyfry: `1`, `2`, `3`, `4`. Przydadzą się na przykład do obliczenia sumy cyfr.

W tej lekcji przyjmujemy liczby całkowite nieujemne. Ujemne liczby wymagają osobnego ustalenia, co zrobić ze znakiem minus. Nie należą do podstawowego algorytmu. Przy odczycie przez `int(input())` zakładamy poprawny zapis liczby całkowitej. Sprawdzamy jej znak.

## Przykład ręczny

Ostatnia cyfra to reszta z dzielenia przez `10`. Zapis `1234 % 10` daje `4`. Dzielenie całkowite `1234 // 10` daje `123`, czyli usuwa ostatnią cyfrę.

| Liczba | Ostatnia cyfra | Liczba po usunięciu cyfry |
| --- | --- | --- |
| 1234 | 4 | 123 |
| 123 | 3 | 12 |
| 12 | 2 | 1 |
| 1 | 1 | 0 |

Otrzymujemy kolejno `4`, `3`, `2`, `1`. Zaczynamy od prawej strony, ponieważ reszta z dzielenia przez `10` dotyczy miejsca jedności. Po jego usunięciu dawna cyfra dziesiątek trafia na koniec.

Nie sortujemy cyfr. Sortowanie zmieniłoby ich kolejność według wartości, a nie według położenia w liczbie.

## Algorytm słownie

1. Odrzuć liczbę ujemną.
2. Dla zera wypisz jedną cyfrę `0`.
3. Dla liczby dodatniej przygotuj kopię do dalszego dzielenia.
4. Dopóki kopia jest większa od zera, odczytaj ostatnią cyfrę i wypisz ją.
5. Usuń ostatnią cyfrę przez dzielenie całkowite przez `10`.
6. Wróć do sprawdzenia warunku pętli.

W każdym obiegu dodatnia liczba staje się mniejsza. Po ostatniej cyfrze zostaje zero. Dlatego pętla się kończy.

## Implementacja: cyfry od końca

Dane przykładowe: jeden wiersz z liczbą `1234`. `input()` bez komunikatu niczego nie wypisuje.

<details markdown="1">
<summary>Pokaż implementację - cyfry od końca</summary>

```python
liczba = int(input())
if liczba < 0:
    print("Błąd danych")
elif liczba == 0:
    print(0)
else:
    pozostalaLiczba = liczba
    while pozostalaLiczba > 0:
        cyfra = pozostalaLiczba % 10
        print(cyfra)
        pozostalaLiczba = pozostalaLiczba // 10
```

Wynik dla `1234`:

```text
4
3
2
1
```

</details>

## Jak czytać kod?

`liczba` zachowuje dane wejściowe. `pozostalaLiczba` zmienia się podczas dzielenia. Dzięki temu nie tracimy oryginalnej wartości.

`cyfra` przechowuje tylko ostatnią cyfrę bieżącej liczby. Po jej odczycie wykonujemy `// 10`. Użycie zwykłego `/` tworzyłoby wynik z częścią ułamkową i nie realizowałoby tego algorytmu.

Dla `7` pętla wykona się raz. Dla `1002` odczyta kolejno `2`, `0`, `0`, `1`. Zera wewnątrz liczby też są cyframi.

## Lista w naturalnej kolejności

Możemy zapisywać cyfry w liście. `append()` dawałoby listę `[4, 3, 2, 1]`. Aby otrzymać naturalną kolejność, wstawiamy każdą nową cyfrę na początek przez `insert(0, cyfra)`.

| Odczytana cyfra | Lista po wstawieniu na początek |
| --- | --- |
| 4 | `[4]` |
| 3 | `[3, 4]` |
| 2 | `[2, 3, 4]` |
| 1 | `[1, 2, 3, 4]` |

Dane przykładowe: `1234`.

<details markdown="1">
<summary>Pokaż implementację - lista cyfr</summary>

```python
liczba = int(input())
if liczba < 0:
    print("Błąd danych")
else:
    cyfry = []
    pozostalaLiczba = liczba
    if pozostalaLiczba == 0:
        cyfry.append(0)
    while pozostalaLiczba > 0:
        cyfra = pozostalaLiczba % 10
        cyfry.insert(0, cyfra)
        pozostalaLiczba = pozostalaLiczba // 10
    print(cyfry)
```

Wynik:

```text
[1, 2, 3, 4]
```

</details>

To prosta wersja dla początkujących. Wstawianie na początek przesuwa dotychczasowe elementy. Przy bardzo długich danych istnieją wydajniejsze sposoby, ale nie są tutaj potrzebne.

## Zero i ograniczenia

Zero ma jedną cyfrę: `0`. Sama pętla z warunkiem `pozostalaLiczba > 0` nie wykona się dla zera ani razu. Dlatego potrzebny jest osobny przypadek, dający `[0]`.

Liczba całkowita nie przechowuje zer wiodących. Zapis odczytany jako liczba `0012` ma wartość `12`. Zachowanie początkowych zer będzie tematem następnej lekcji o napisach.

## Typowe błędy

- Pomylenie `% 10` z `// 10`.
- Użycie `/` zamiast `//`.
- Brak zmiany liczby w pętli.
- Przyjęcie, że cyfry odczytujemy od lewej strony.
- Pominięcie osobnego przypadku zera.
- Próba używania podstawowego algorytmu dla liczb ujemnych.

## Ćwiczenia

### Ćwiczenie 1. Ostatnia cyfra

Bez zamiany na napis wypisz ostatnią cyfrę liczby `507`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Pomyśl, jaka część liczby zostaje po podziale na pełne dziesiątki.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
liczba = 507
cyfra = liczba % 10
print(cyfra)
```

Wynik:

```text
7
```

</details>

### Ćwiczenie 2. Usuń cyfrę

Bez użycia napisu usuń ostatnią cyfrę liczby `507`. Wypisz pozostałą wartość.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Potrzebujesz liczby pełnych dziesiątek, a nie reszty.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
liczba = 507
pozostalaLiczba = liczba // 10
print(pozostalaLiczba)
```

Wynik:

```text
50
```

</details>

### Ćwiczenie 3. Suma cyfr

Wczytaj nieujemną liczbę całkowitą. Wypisz sumę jej cyfr. Nie zamieniaj liczby na napis. Dla zera suma wynosi zero. Liczbę ujemną odrzuć komunikatem `Błąd danych`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Kolejność dodawania cyfr nie zmienia sumy. Potrzebujesz akumulatora przygotowanego przed pętlą.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
liczba = int(input())
if liczba < 0:
    print("Błąd danych")
else:
    sumaCyfr = 0
    pozostalaLiczba = liczba
    while pozostalaLiczba > 0:
        sumaCyfr = sumaCyfr + pozostalaLiczba % 10
        pozostalaLiczba = pozostalaLiczba // 10
    print(sumaCyfr)
```

Dla danych `1203` wynik:

```text
6
```

</details>

### Ćwiczenie 4. Liczba cyfr

Wczytaj nieujemną liczbę całkowitą i policz jej cyfry bez napisu. Dla `0` wynik ma wynosić `1`. Liczbę ujemną odrzuć.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Dla liczby dodatniej każdy obieg usuwa jedną cyfrę. Zero wymaga osobnego ustalenia wyniku.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
liczba = int(input())
if liczba < 0:
    print("Błąd danych")
else:
    liczbaCyfr = 0
    pozostalaLiczba = liczba
    if pozostalaLiczba == 0:
        liczbaCyfr = 1
    while pozostalaLiczba > 0:
        liczbaCyfr = liczbaCyfr + 1
        pozostalaLiczba = pozostalaLiczba // 10
    print(liczbaCyfr)
```

Dla danych `1002` wynik:

```text
4
```

</details>

### Ćwiczenie 5. Zera wewnątrz liczby

Wczytaj nieujemną liczbę. Wypisz listę cyfr w naturalnej kolejności. Sprawdź dane `1002` i `0`. Nie używaj `str()`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Nowo odczytana cyfra pochodzi z lewej strony już odczytanej części. Zastanów się, gdzie umieścić ją w liście.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
liczba = int(input())
if liczba < 0:
    print("Błąd danych")
else:
    cyfry = []
    pozostalaLiczba = liczba
    if pozostalaLiczba == 0:
        cyfry.append(0)
    while pozostalaLiczba > 0:
        cyfry.insert(0, pozostalaLiczba % 10)
        pozostalaLiczba = pozostalaLiczba // 10
    print(cyfry)
```

Dla danych `1002` wynik:

```text
[1, 0, 0, 2]
```

Dla zera wynik to `[0]`.

</details>

## Podsumowanie

`% 10` odczytuje ostatnią cyfrę, a `// 10` ją usuwa. Cyfry dostajemy od prawej do lewej. Osobno obsługujemy zero. Do zachowania zer wiodących potrzebny jest napis, a nie sama wartość liczbowa.
