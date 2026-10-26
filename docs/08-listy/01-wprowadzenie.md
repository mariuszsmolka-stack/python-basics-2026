---
layout: default
title: Czym jest lista?
---

# Czym jest lista?

## Cel lekcji

Zrozumiesz, po co przechowywać kilka wartości w jednej liście. Utworzysz pierwsze listy i sprawdzisz liczbę ich elementów.

## Czego się nauczysz

- Rozpoznawać element listy.
- Tworzyć listę pustą, listę liczb i listę napisów.
- Wypisywać całą listę.
- Odróżniać liczbę elementów od numeru ostatniej pozycji.

## Po co nam lista?

Możesz zapisać cztery oceny w zmiennych `pierwszaOcena`, `drugaOcena`, `trzeciaOcena` i `czwartaOcena`. Przy czterdziestu ocenach takie nazwy stają się niewygodne.

**Lista jest uporządkowaną kolekcją elementów.** Element to jedna przechowywana wartość. Uporządkowanie oznacza, że elementy mają swoje pozycje. Nie oznacza, że liczby są ustawione od najmniejszej do największej.

Listę zapisujemy w nawiasach kwadratowych `[]`. Elementy oddzielamy przecinkami. Nazwa zmiennej, na przykład `oceny`, pozwala później korzystać z całej listy. Ta sama wartość może wystąpić kilka razy.

## Pierwszy przykład

```python
oceny = [3, 4, 5, 4]
print(oceny)
print(len(oceny))
```

Wynik:

```text
[3, 4, 5, 4]
4
```

## Omówienie działania programu

1. Pierwszy wiersz tworzy listę z czterema elementami.
2. `print(oceny)` wypisuje całą listę. Widzimy nawiasy i elementy w ich kolejności.
3. Wbudowana funkcja `len()` podaje liczbę elementów. `len(oceny)` oznacza: policz elementy listy `oceny`.
4. Drugie wystąpienie oceny `4` też jest osobnym elementem. Dlatego długość wynosi `4`, a nie `3`.

## Lista pusta

Lista może na razie nie zawierać żadnych elementów. Nadal jest listą. W późniejszej lekcji nauczysz się ją uzupełniać.

```python
listaZakupow = []
print(listaZakupow)
print(len(listaZakupow))
```

Wynik:

```text
[]
0
```

Nie wpisujemy do pustej listy zera. Lista `[]` ma zero elementów, a lista `[0]` ma jeden element o wartości zero.

## Lista napisów i różne typy

Napis jest tekstem, więc zapisujemy go w cudzysłowie.

```python
imiona = ["Ala", "Olek", "Maja"]
print(imiona)
print(len(imiona))
```

Wynik:

```text
['Ala', 'Olek', 'Maja']
3
```

Python może przy wypisywaniu napisów użyć apostrofów zamiast podwójnych cudzysłowów. To nadal te same napisy.

Lista może zawierać elementy różnych typów:

```python
daneUcznia = ["Ala", 16, True]
print(daneUcznia)
```

Wynik:

```text
['Ala', 16, True]
```

W pierwszych ćwiczeniach wybieramy listy jednorodne, na przykład same liczby albo same napisy. Łatwiej wtedy przewidzieć dozwolone działania.

## Długość a indeks

**Indeks** to numer pozycji elementu. Python liczy pozycje od zera. Dokładny odczyt elementu poznasz w następnej lekcji.

| Lista | Długość z `len()` | Indeksy liczone od zera | Ostatni nieujemny indeks |
| --- | --- | --- | --- |
| `[3, 4, 5, 4]` | 4 | 0, 1, 2, 3 | 3 |
| `[8]` | 1 | 0 | 0 |
| `[]` | 0 | brak | brak |

Dla niepustej listy ostatni nieujemny indeks jest o jeden mniejszy od długości. Sama długość nie jest poprawnym indeksem. Pusta lista nie ma ostatniego elementu.

## Typowe błędy

- `[]` oraz `[0]` nie oznaczają tego samego.
- Wartość `5` i napis `"5"` to różne typy danych.
- Kolejność elementów nie oznacza automatycznego sortowania.
- Powtórzenia również zwiększają długość listy.
- Do `len()` przekazujemy nazwę listy. Napis `"oceny"` byłby inną daną - tekstem z pięciu znaków.

## Ćwiczenia

### Ćwiczenie 1. Trzy oceny

Utwórz listę `oceny` z wartościami `2`, `4`, `5`. Wypisz całą listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Zapisz wszystkie wartości między jedną parą nawiasów kwadratowych. Zachowaj kolejność.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
oceny = [2, 4, 5]
print(oceny)
```

Wynik:

```text
[2, 4, 5]
```

</details>

### Ćwiczenie 2. Pusty plan

Utwórz pustą listę `planDnia`. Wypisz ją oraz jej długość w osobnych wierszach.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

W pustej liście nie zapisujesz żadnej wartości, nawet zera.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
planDnia = []
print(planDnia)
print(len(planDnia))
```

Wynik:

```text
[]
0
```

</details>

### Ćwiczenie 3. Przedmioty

Utwórz listę `przedmioty` z napisami `"matematyka"`, `"polski"`, `"informatyka"`. Wypisz listę i jej długość.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Każda nazwa jest osobnym napisem. Liczymy przedmioty, a nie litery w ich nazwach.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
przedmioty = ["matematyka", "polski", "informatyka"]
print(przedmioty)
print(len(przedmioty))
```

Wynik:

```text
['matematyka', 'polski', 'informatyka']
3
```

</details>

### Ćwiczenie 4. Powtórzenia

Utwórz listę `wyniki` z wartościami `7`, `7`, `2`, `7`. Wypisz liczbę elementów. Czy powtarzająca się siódemka jest liczona tylko raz?

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Każda pozycja zawiera osobny element. Równe wartości mogą zajmować różne pozycje.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
wyniki = [7, 7, 2, 7]
print(len(wyniki))
```

Wynik:

```text
4
```

Wszystkie trzy siódemki są liczone. Lista ma cztery elementy.

</details>

### Ćwiczenie 5. Długość i ostatnia pozycja

Utwórz listę `temperatury` z wartościami `12`, `15`, `14`, `11`, `10`. Wypisz jej długość. Osobno oblicz i wypisz ostatni nieujemny indeks. Ta lista jest niepusta.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Numerowanie zaczyna się od zera. Porównaj liczbę elementów z numerem ostatniej pozycji w tabeli.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
temperatury = [12, 15, 14, 11, 10]
liczbaPomiarow = len(temperatury)
ostatniIndeks = liczbaPomiarow - 1
print(liczbaPomiarow)
print(ostatniIndeks)
```

Wynik:

```text
5
4
```

</details>

## Podsumowanie

Lista przechowuje elementy w określonej kolejności. Nawiasy `[]` wyznaczają listę, a `len()` podaje liczbę jej elementów. Długość i indeks ostatniego elementu to różne liczby.
