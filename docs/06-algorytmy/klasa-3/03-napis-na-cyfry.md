---
layout: default
title: Zamiana napisu na cyfry
---

# Zamiana napisu na cyfry

## Cel lekcji

Odróżnisz liczbę od jej tekstowego zapisu. Zamienisz kolejne znaki poprawnego napisu na cyfry typu `int`.

## Problem po ludzku

`1234` jest liczbą całkowitą. `"1234"` jest napisem, czyli ciągiem znaków. Wyglądają podobnie, ale dopuszczają inne działania. Po napisie możemy przechodzić pętlą `for`.

Znak `"1"` to tekst. Liczba `1` to wartość całkowita. Wbudowane `int(znak)` zamienia pojedynczy znak cyfry na liczbę. Nie oznacza to jeszcze odczytania całego zapisu w systemie dwójkowym.

## Rozwiązanie ręczne

Dla napisu `"1234"` bierzemy znaki od lewej strony:

| Znak | Po zamianie przez `int()` | Lista po dopisaniu |
| --- | --- | --- |
| `"1"` | 1 | `[1]` |
| `"2"` | 2 | `[1, 2]` |
| `"3"` | 3 | `[1, 2, 3]` |
| `"4"` | 4 | `[1, 2, 3, 4]` |

Tym razem naturalna kolejność pojawia się od razu. Nie dzielimy liczby i nie usuwamy jej ostatniej cyfry.

## Algorytm słownie

Dla znanego, poprawnego napisu przejdź kolejno po znakach. Zamień każdy znak na cyfrę. Wypisz ją lub dopisz do listy. Pętla `for` kończy się po ostatnim znaku.

## Implementacja: wypisanie cyfr

Ten pierwszy przykład ma stałe, poprawne dane. Każdy wiersz wyniku zawiera liczbę, nie napis.

<details markdown="1">
<summary>Pokaż implementację - znaki i cyfry</summary>

```python
zapisLiczby = "1234"
for znak in zapisLiczby:
    cyfra = int(znak)
    print(cyfra)
```

Wynik:

```text
1
2
3
4
```

</details>

`znak` otrzymuje kolejno teksty `"1"`, `"2"`, `"3"`, `"4"`. `cyfra` otrzymuje ich wartości całkowite. `print()` może pokazywać je podobnie, ale ich typy są różne.

## Zera wiodące i system liczbowy

Napis `"0012"` ma cztery znaki. Jako lista cyfr daje `[0, 0, 1, 2]`. Zamiana całego napisu przez `int("0012")` dałaby liczbę `12` i nie zachowałaby informacji o dwóch początkowych zerach.

Napis `"1011"` daje listę `[1, 0, 1, 1]`. Samo wyodrębnienie cyfr nie mówi, czy chodzi o zapis dziesiętny, czy dwójkowy. Jako liczba dziesiętna ma wartość `1011`, a jako dwójkowa wartość `11`. Odczytywanie wartości pozycyjnej poznamy w kolejnych lekcjach.

## Dane od użytkownika wymagają kontroli

Pusty napis nie zawiera żadnej cyfry. Nie uznajemy go za poprawny zapis liczby. Litera, spacja i znak minus także nie należą do przyjętego formatu.

W tej lekcji akceptujemy wyłącznie znaki `0`, `1`, ..., `9`, także z zerami na początku. `znak in "0123456789"` sprawdza obecność znaku w tym napisie. Zapis `not in` oznacza brak znaku. Działa podobnie do poznanego sprawdzania obecności elementu w liście.

Najpierw sprawdzamy cały napis. Dopiero po udanej kontroli wykonujemy zamianę znaków. Nie pomijamy błędnych znaków po cichu.

1. Ustaw informację o poprawności na podstawie niepustej długości.
2. Sprawdź każdy znak. Niedozwolony znak ustawia informację o błędzie.
3. Jeśli napis jest poprawny, utwórz listę i dopisz do niej kolejne cyfry.
4. W przeciwnym razie wypisz `Błąd danych`.

## Implementacja: sprawdzona lista cyfr

Dane przykładowe: jeden wiersz `0014`.

<details markdown="1">
<summary>Pokaż implementację - kontrola i lista cyfr</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
if czyPoprawny:
    cyfry = []
    for znak in zapisLiczby:
        cyfra = int(znak)
        cyfry.append(cyfra)
    print(cyfry)
else:
    print("Błąd danych")
```

Wynik:

```text
[0, 0, 1, 4]
```

</details>

## Dlaczego są dwie pętle?

Pierwsza sprawdza format. Druga przetwarza już sprawdzone dane. Dzięki temu `int(znak)` nie dostanie litery ani spacji.

Nie ustawiamy `czyPoprawny` ponownie na `True` po napotkaniu dozwolonego znaku. Jeden błąd ma pozostać zapamiętany do końca kontroli. Samo `if czyPoprawny` oznacza: wykonaj gałąź, jeżeli ta zmienna logiczna ma wartość `True`.

## Typowe błędy

- Traktowanie `"1"` jak liczby `1` bez konwersji.
- Zamiana całego napisu na `int`, gdy trzeba zachować zera wiodące.
- Założenie, że pętla sprawdzająca znaki sama odrzuci pusty napis. Dla niego nie wykona się ani razu.
- Wywołanie `int()` na literze. Spowodowałoby to `ValueError`.
- Mylenie listy cyfr z obliczeniem wartości liczby w danej podstawie.

## Ćwiczenia

### Ćwiczenie 1. Stały napis

Zamień stały, poprawny napis `"507"` na listę cyfr całkowitych. Wypisz listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Kolejność znaków jest już właściwa. Każdy znak wymaga osobnej zamiany na liczbę.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
zapisLiczby = "507"
cyfry = []
for znak in zapisLiczby:
    cyfry.append(int(znak))
print(cyfry)
```

Wynik:

```text
[5, 0, 7]
```

</details>

### Ćwiczenie 2. Początkowe zera

Wczytaj niepusty napis złożony wyłącznie z cyfr od `0` do `9`. Wypisz listę cyfr i jej długość. Błędny zapis odrzuć. Sprawdź `0012`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Długość zapisu nie musi być taka sama jak liczba cyfr po odczytaniu go jako jednej liczby całkowitej.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
if czyPoprawny:
    cyfry = []
    for znak in zapisLiczby:
        cyfry.append(int(znak))
    print(cyfry)
    print(len(cyfry))
else:
    print("Błąd danych")
```

Dla `0012` wynik:

```text
[0, 0, 1, 2]
4
```

</details>

### Ćwiczenie 3. Suma cyfr napisu

Wczytaj i sprawdź napis cyfr dziesiętnych. Wypisz sumę ich wartości. Dla `1011` suma ma wynosić `3`. Nie jest to konwersja liczby dwójkowej.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Dodajesz wartości pojedynczych cyfr. Nie dodawaj do siebie napisów i nie obliczaj wartości pozycyjnej całej liczby.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
if czyPoprawny:
    sumaCyfr = 0
    for znak in zapisLiczby:
        sumaCyfr = sumaCyfr + int(znak)
    print(sumaCyfr)
else:
    print("Błąd danych")
```

Dla `1011` wynik:

```text
3
```

</details>

### Ćwiczenie 4. Samo sprawdzenie formatu

Wczytaj napis. Wypisz `Poprawny zapis` wyłącznie dla niepustego ciągu znaków od `0` do `9`. W pozostałych przypadkach wypisz `Błąd danych`. Sprawdź pusty wiersz i `12a`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Osobno uwzględnij długość i dozwolone znaki. Wynik ma zostać odrzucony po choć jednym błędzie.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
if czyPoprawny:
    print("Poprawny zapis")
else:
    print("Błąd danych")
```

Dla `12a` wynik:

```text
Błąd danych
```

</details>

### Ćwiczenie 5. Pierwsza i ostatnia cyfra

Wczytaj poprawny niepusty napis cyfr. Zamień go na listę i wypisz pierwszą oraz ostatnią cyfrę jako liczby. Błędne dane odrzuć. Sprawdź `0012`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Po sprawdzeniu niepustego napisu lista też będzie niepusta. Dopiero wtedy wolno odczytywać jej krańcowe elementy.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
if czyPoprawny:
    cyfry = []
    for znak in zapisLiczby:
        cyfry.append(int(znak))
    print(cyfry[0])
    print(cyfry[-1])
else:
    print("Błąd danych")
```

Dla `0012` wynik:

```text
0
2
```

</details>

## Podsumowanie

Napis zachowuje kolejność znaków i zera wiodące. Pojedyncze znaki zamieniamy na `int`, ale dopiero po sprawdzeniu formatu. Lista cyfr i wartość liczby w określonej podstawie to różne wyniki.
