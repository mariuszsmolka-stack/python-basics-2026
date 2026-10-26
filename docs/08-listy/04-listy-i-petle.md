---
layout: default
title: Listy i pętle
---

# Listy i pętle

## Cel lekcji

Połączysz znaną pętlę `for` z listą. Nauczysz się czytać elementy, zmieniać je przez indeks oraz budować listę w pętli.

## Czego się nauczysz

- Wybierać między przechodzeniem po wartościach a przechodzeniem po indeksach.
- Wypisywać elementy w osobnych wierszach.
- Zmieniać wartości na istniejących pozycjach.
- Dodawać kolejne dane przez `append()`.
- Wczytywać kilka liczb do listy.

## Dwa sposoby przechodzenia przez listę

Wcześniej pętla `for` pobierała liczby z `range()`. Może też pobierać kolejne wartości z listy. Jeden obieg pętli to wykonanie jej wciętych instrukcji dla jednego elementu.

Gdy wystarcza sama wartość, wybierz `for element in lista`. Gdy potrzebujesz numeru pozycji lub chcesz zmieniać element na tej pozycji, możesz użyć `range(len(lista))`.

## Pierwszy przykład: wartości elementów

```python
liczby = [10, 20, 30]
for liczba in liczby:
    print(liczba)
```

Wynik:

```text
10
20
30
```

## Omówienie działania programu

1. Tworzymy listę z trzema liczbami.
2. Pętla pobiera pierwszy element. Zmienna `liczba` ma wartość `10`.
3. Wcięty `print()` wypisuje tę wartość.
4. Potem `liczba` otrzymuje `20`, a następnie `30`. Dla każdej wartości wykonuje się `print()`.
5. Po ostatnim elemencie pętla się kończy.

| Obieg pętli | Wartość zmiennej `liczba` | Wypisana wartość |
| --- | --- | --- |
| 1 | 10 | 10 |
| 2 | 20 | 20 |
| 3 | 30 | 30 |

Zmienna `liczba` przechowuje tutaj element, a nie indeks. Nie należy odczytywać `liczby[liczba]`: próbowalibyśmy wtedy użyć indeksu `10`, potem `20` i `30`.

## Drugi sposób: indeksy

`len(liczby)` wynosi `3`. Zatem `range(len(liczby))` daje indeksy `0`, `1`, `2`. Przez `liczby[indeks]` odczytujemy element z danej pozycji.

```python
liczby = [10, 20, 30]
for indeks in range(len(liczby)):
    print(liczby[indeks])
```

Wynik jest taki sam:

```text
10
20
30
```

Różnica tkwi w zmiennej pętli. W poprzednim programie miała wartości `10`, `20`, `30`. Teraz ma wartości `0`, `1`, `2`.

Dzięki indeksom możemy wypisać jednocześnie pozycję i wartość:

```python
oceny = [3, 5, 4]
for indeks in range(len(oceny)):
    print(indeks, oceny[indeks])
```

Wynik:

```text
0 3
1 5
2 4
```

Nie używaj indeksów tylko dlatego, że to możliwe. Do samego wypisania wartości pierwszy sposób jest krótszy i czytelniejszy. Oba sposoby dla pustej listy wykonają zero obiegów.

## Zmiana wartości listy

Przypisanie do `liczby[indeks]` zmienia element listy. Tutaj zwiększamy każdy element o jeden:

```python
liczby = [2, 4, 6]
for indeks in range(len(liczby)):
    liczby[indeks] = liczby[indeks] + 1
print(liczby)
```

Wynik:

```text
[3, 5, 7]
```

| `indeks` | Wartość przed zmianą | Wartość po zmianie |
| --- | --- | --- |
| 0 | 2 | 3 |
| 1 | 4 | 5 |
| 2 | 6 | 7 |

Wcięta instrukcja zmienia jeden element w każdym obiegu. `print()` po pętli wypisuje dopiero końcową listę.

Samo przypisanie do zmiennej pętli nie zmienia elementu listy liczb:

```python
liczby = [2, 4, 6]
for liczba in liczby:
    liczba = liczba + 1
print(liczby)
```

Wynik:

```text
[2, 4, 6]
```

Zmieniliśmy tylko wartość zmiennej `liczba`. Nie zapisaliśmy wyniku na żadnej pozycji listy. To ważna różnica.

## Budowanie nowej listy

Zaczynamy od pustej listy. W każdym obiegu dodajemy do niej jeden wynik. Lista źródłowa zostaje bez zmian.

```python
liczby = [2, 4, 6]
podwojoneLiczby = []
for liczba in liczby:
    podwojoneLiczby.append(liczba * 2)
print(liczby)
print(podwojoneLiczby)
```

Wynik:

```text
[2, 4, 6]
[4, 8, 12]
```

Przed pętlą lista wynikowa jest pusta. Po pierwszym obiegu zawiera `[4]`, po drugim `[4, 8]`, a po trzecim `[4, 8, 12]`.

## Wczytywanie danych

Pierwszy wiersz danych określa, ile liczb wczytamy. Następne wiersze zawierają po jednej liczbie całkowitej. Zakładamy poprawne liczby oraz nieujemną liczbę elementów. `input()` bez komunikatu niczego nie wypisuje. To użytkownik wpisuje dane i zatwierdza je klawiszem Enter.

Dla tego przykładu wpisz kolejno:

```text
3
8
2
5
```

```python
liczbaElementow = int(input())
liczby = []
for numerElementu in range(liczbaElementow):
    liczba = int(input())
    liczby.append(liczba)
print(liczby)
```

Wynik programu, bez powtarzania wpisanych danych:

```text
[8, 2, 5]
```

Pierwsze `3` określa liczbę obiegów. Nie trafia do listy. W każdym obiegu `input()` odczytuje kolejną daną, `int()` zamienia ją na liczbę, a `append()` dodaje ją na końcu. Gdy jako liczbę elementów podasz `0`, program od razu wypisze `[]`.

## Typowe błędy

- Element nie musi być równy swojemu indeksowi.
- `range(len(lista) + 1)` daje jeden indeks za dużo.
- Przypisanie do zmiennej pętli nie zmienia listy liczb.
- Nową listę tworzymy przed pętlą. Tworzenie jej od nowa w każdym obiegu zgubi wcześniejsze wyniki.
- `input()` zwraca tekst. Do obliczeń na liczbach potrzebujesz konwersji.
- Podczas przechodzenia po liście nie usuwaj z niej elementów ani nie dopisuj do tej samej listy. Zmienia to przebieg pętli. W tym dziale budujemy wtedy osobną listę wynikową.

## Ćwiczenia

### Ćwiczenie 1. Imiona w wierszach

Wypisz elementy `imiona = ["Ala", "Olek", "Ewa"]` w osobnych wierszach. Przechodź po wartościach, bez indeksów.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Potrzebujesz samego imienia. Jeden obieg ma wypisać jedną osobę.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
imiona = ["Ala", "Olek", "Ewa"]
for imie in imiona:
    print(imie)
```

Wynik:

```text
Ala
Olek
Ewa
```

</details>

### Ćwiczenie 2. Pozycja i wynik

Dla `wyniki = [7, 9, 6]` wypisz w każdym wierszu indeks oraz wartość, rozdzielone spacją.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Tym razem potrzebujesz również pozycji. Długość listy określa koniec zakresu indeksów.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
wyniki = [7, 9, 6]
for indeks in range(len(wyniki)):
    print(indeks, wyniki[indeks])
```

Wynik:

```text
0 7
1 9
2 6
```

</details>

### Ćwiczenie 3. Dodatkowe punkty

Zwiększ każdy element listy `punkty = [1, 3, 5]` o `2`. Zmień istniejącą listę i wypisz ją po pętli.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Nową wartość trzeba zapisać na odpowiedniej pozycji listy, a nie tylko w zmiennej pętli.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
punkty = [1, 3, 5]
for indeks in range(len(punkty)):
    punkty[indeks] = punkty[indeks] + 2
print(punkty)
```

Wynik:

```text
[3, 5, 7]
```

</details>

### Ćwiczenie 4. Trzy odczyty

Wczytaj dokładnie trzy liczby całkowite, każdą w osobnym wierszu. Zbuduj listę i wypisz ją. Przykładowe dane to `8`, `2`, `5`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Liczba powtórzeń jest znana. Każdy odczyt dostarcza jeden nowy element.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
liczby = []
for numerElementu in range(3):
    liczba = int(input())
    liczby.append(liczba)
print(liczby)
```

Dla danych `8`, `2`, `5` wynik to:

```text
[8, 2, 5]
```

</details>

### Ćwiczenie 5. Kwadraty

Zbuduj listę kwadratów liczb od `1` do `4`. Kwadrat liczby to ta liczba pomnożona przez siebie. Wypisz listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Pętla może pobierać liczby z zakresu. Do listy wynikowej dodawaj obliczoną wartość.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
kwadraty = []
for liczba in range(1, 5):
    kwadraty.append(liczba * liczba)
print(kwadraty)
```

Wynik:

```text
[1, 4, 9, 16]
```

</details>

### Ćwiczenie 6. Tylko dodatnie

Z listy `liczby = [2, -1, 0, 5, -3]` przepisz do nowej listy `dodatnieLiczby` tylko wartości większe od zera. Zachowaj ich kolejność. Wypisz nową listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 6</summary>

Sprawdzaj warunek dla każdego elementu. Nie każda wartość musi zostać dopisana do wyniku.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 6</summary>

```python
liczby = [2, -1, 0, 5, -3]
dodatnieLiczby = []
for liczba in liczby:
    if liczba > 0:
        dodatnieLiczby.append(liczba)
print(dodatnieLiczby)
```

Wynik:

```text
[2, 5]
```

</details>

## Podsumowanie

Wartość elementu wystarcza do odczytu i wielu obliczeń. Indeks przydaje się do pracy z pozycją i zmiany listy. Nowe dane można zbierać w osobnej liście przez `append()` w pętli.
