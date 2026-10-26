---
layout: default
title: System dwójkowy na dziesiętny
---

# System dwójkowy na dziesiętny

## Cel lekcji

Odczytasz wartość niepustego napisu dwójkowego. Zrozumiesz, dlaczego aktualizujemy wynik przez mnożenie przez dwa i dodanie kolejnej cyfry.

## Problem po ludzku

Napis `"1101"` nie oznacza tutaj tysiąca stu jeden. Umawiamy się, że to zapis w systemie dwójkowym. Dozwolone są wyłącznie cyfry `0` i `1`.

`1101` dwójkowo => `13` dziesiętnie.

Nie zamieniamy całego napisu na liczbę na początku. Najpierw sprawdzamy znaki, a potem przetwarzamy je od lewej do prawej.

## Wartości pozycji: przykład ręczny

Od prawej strony kolejne pozycje mają wartości `1`, `2`, `4`, `8`. Każda następna pozycja jest dwa razy większa.

| Pozycja od lewej | Cyfra | Wartość pozycji | Wkład do liczby |
| --- | --- | --- | --- |
| pierwsza | 1 | 8 | 1 * 8 = 8 |
| druga | 1 | 4 | 1 * 4 = 4 |
| trzecia | 0 | 2 | 0 * 2 = 0 |
| czwarta | 1 | 1 | 1 * 1 = 1 |

Suma: `8 + 4 + 0 + 1 = 13`.

## Wygodniejszy sposób liczenia od lewej

Zaczynamy od wyniku `0`. Przed dołączeniem kolejnej cyfry mnożymy dotychczasowy wynik przez `2`. Następnie dodajemy wartość nowej cyfry.

`wynik = wynik * 2 + cyfra`

| Cyfra | Obliczenie | Wynik |
| --- | --- | --- |
| 1 | 0 * 2 + 1 | 1 |
| 1 | 1 * 2 + 1 | 3 |
| 0 | 3 * 2 + 0 | 6 |
| 1 | 6 * 2 + 1 | 13 |

Po dwóch znakach odczytaliśmy `11`, czyli `3`. Dołączenie zera tworzy `110`. Dawne cyfry przesuwają się o jedną pozycję, więc ich łączna wartość podwaja się: `3 * 2 = 6`. Ostatnia jedynka daje `6 * 2 + 1 = 13`.

To ten sam pomysł co dopisanie cyfry w systemie dziesiętnym, gdzie poprzednią wartość mnożylibyśmy przez `10`. Tutaj podstawa wynosi `2`.

## Sprawdzenie danych

Pusty napis odrzucamy. Nie traktujemy go jak zera. Poprawny zapis zera to `"0"`, a także na przykład `"000"`.

Każdy znak musi być równy `"0"` lub `"1"`. Zapis `"102"` jest błędny. Nie wolno pominąć dwójki i obliczyć wyniku z pozostałej części.

## Algorytm słownie

1. Sprawdź, czy napis jest niepusty.
2. Sprawdź wszystkie znaki. Zapamiętaj każdy błąd.
3. Jeżeli dane są błędne, wypisz komunikat i nie wykonuj konwersji.
4. Dla poprawnych danych ustaw wynik na zero.
5. Przechodź po znakach od lewej do prawej.
6. Zamieniaj pojedynczy znak na cyfrę. Aktualizuj wynik według poznanej zależności.
7. Wypisz wartość dziesiętną.

## Implementacja w Pythonie

Dane przykładowe: `1101`.

<details markdown="1">
<summary>Pokaż implementację - dwójkowy na dziesiętny</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak != "0" and znak != "1":
        czyPoprawny = False
if czyPoprawny:
    wynik = 0
    for znak in zapisLiczby:
        cyfra = int(znak)
        wynik = wynik * 2 + cyfra
    print(wynik)
else:
    print("Błąd danych")
```

Wynik:

```text
13
```

</details>

## Wyjaśnienie kodu

Pierwsza pętla sprawdza dane. Warunek błędu oznacza: znak nie jest ani zerem, ani jedynką. Jedno znalezione naruszenie wystarcza do odrzucenia całego napisu.

Dopiero druga pętla wykonuje obliczenia. `int(znak)` zamienia jeden sprawdzony znak na `0` albo `1`. Nie wykonuje gotowej konwersji całego zapisu.

Początkowe zera nie zmieniają wartości. Dla `00101` pierwsze dwa kroki pozostawiają wynik równy zero, a następne dają kolejno `1`, `2`, `5`.

## Typowe błędy

- Dodawanie samych cyfr, zamiast uwzględniania ich pozycji.
- Mnożenie przez `10`, mimo że podstawa wynosi `2`.
- Czytanie od prawej przy zastosowaniu algorytmu przeznaczonego do czytania od lewej.
- Uznawanie każdego znaku dziesiętnego za poprawny znak dwójkowy.
- Zerowanie wyniku w każdym obiegu.
- Ciche pomijanie nieprawidłowych znaków lub pustego wejścia.

## Ćwiczenia

### Ćwiczenie 1. Pięć ręcznie

Oblicz ręcznie dziesiętną wartość zapisu dwójkowego `101`. Pokaż zarówno wartości pozycji, jak i kolejne wyniki przy czytaniu od lewej.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Kolejne wartości pozycji od prawej to jeden, dwa i cztery. Przy czytaniu od lewej pamiętaj o przesunięciu poprzednich cyfr.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

Z wartości pozycji: `1 * 4 + 0 * 2 + 1 * 1 = 5`.

Kolejne wyniki: `0 * 2 + 1 = 1`, potem `1 * 2 + 0 = 2`, następnie `2 * 2 + 1 = 5`.

</details>

### Ćwiczenie 2. Zera na początku

Wczytaj i sprawdź zapis dwójkowy. Oblicz jego wartość bez gotowej konwersji. Sprawdź `00101`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Zero dodane do dwukrotności zera nadal daje zero. Nie musisz wcześniej usuwać początkowych zer.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "01":
        czyPoprawny = False
if czyPoprawny:
    wynik = 0
    for znak in zapisLiczby:
        wynik = wynik * 2 + int(znak)
    print(wynik)
else:
    print("Błąd danych")
```

Dla `00101` wynik:

```text
5
```

</details>

### Ćwiczenie 3. Błędna cyfra i pusty napis

Sprawdź, czy wejście jest niepustym zapisem dwójkowym. Wypisz `Poprawny zapis` albo `Błąd danych`. Nie wykonuj konwersji. Przetestuj `102` i pusty wiersz.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Poprawność wymaga jednocześnie odpowiedniej długości i odpowiednich znaków. Samo występowanie cyfr dziesiętnych nie wystarcza.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "01":
        czyPoprawny = False
if czyPoprawny:
    print("Poprawny zapis")
else:
    print("Błąd danych")
```

Dla `102` wynik:

```text
Błąd danych
```

</details>

### Ćwiczenie 4. Osiem jedynek

Zapisz program odczytujący poprawny napis dwójkowy jako wartość dziesiętną. Uwzględnij kontrolę danych. Uruchom go dla `11111111` oraz `0`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Nie musisz zmieniać algorytmu dla dłuższego napisu. Każdy kolejny znak aktualizuje ten sam wynik.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "01":
        czyPoprawny = False
if czyPoprawny:
    wynik = 0
    for znak in zapisLiczby:
        wynik = wynik * 2 + int(znak)
    print(wynik)
else:
    print("Błąd danych")
```

Dla `11111111` wynik:

```text
255
```

Dla `0` wynik to `0`.

</details>

### Ćwiczenie 5. Czy to ta sama wartość?

Wczytaj dwa napisy dwójkowe, każdy w osobnym wierszu. Sprawdź oba i porównaj ich wartości liczbowe. Wypisz `True` albo `False`. Dla błędu któregokolwiek napisu wypisz `Błąd danych`. Sprawdź `010` oraz `10`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Różne napisy mogą opisywać tę samą wartość. Porównanie samych tekstów nie wystarczy.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
pierwszyZapis = input()
drugiZapis = input()
czyPoprawny = len(pierwszyZapis) > 0 and len(drugiZapis) > 0
for znak in pierwszyZapis:
    if znak not in "01":
        czyPoprawny = False
for znak in drugiZapis:
    if znak not in "01":
        czyPoprawny = False
if czyPoprawny:
    pierwszyWynik = 0
    for znak in pierwszyZapis:
        pierwszyWynik = pierwszyWynik * 2 + int(znak)
    drugiWynik = 0
    for znak in drugiZapis:
        drugiWynik = drugiWynik * 2 + int(znak)
    print(pierwszyWynik == drugiWynik)
else:
    print("Błąd danych")
```

Dla danych `010` i `10` wynik:

```text
True
```

</details>

## Dopiero teraz: funkcja wbudowana

Po poznaniu algorytmu można skorzystać z `int(zapisLiczby, 2)`. Drugi argument podaje podstawę. Poniższy program używa stałych, poprawnych danych:

<details markdown="1">
<summary>Pokaż porównanie z funkcją wbudowaną</summary>

```python
zapisLiczby = "1101"
print(int(zapisLiczby, 2))
```

Wynik:

```text
13
```

</details>

Gotowa funkcja jest wygodna, lecz nie zastępuje zrozumienia mnożenia przez podstawę i dodawania cyfry. W zadaniach wymagających własnego algorytmu nie używamy jej zamiast pętli.

## Podsumowanie

Czytamy cyfry od lewej strony. Każdy krok przesuwa dotychczasowe cyfry przez mnożenie wyniku przez `2`, a potem dodaje nową cyfrę. Najpierw sprawdzamy cały napis, aby nie obliczać wyniku z błędnych danych.
