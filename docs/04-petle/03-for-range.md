# Pętla for i funkcja range() w Pythonie

## Cel lekcji

Poznasz pętlę `for` oraz funkcję `range()` i nauczysz się powtarzać instrukcje określoną liczbę razy.

## Czego się nauczysz

Po tej lekcji będziesz umieć wypisywać kolejne liczby, korzystać z `range()`, sumować liczby, obliczać iloczyn oraz tworzyć prostą tabliczkę mnożenia dla jednej liczby.

## Po co używamy pętli for

Pętla `for` służy do powtarzania instrukcji określoną liczbę razy.

Zamiast pisać kilka razy podobny kod, możemy napisać jedną pętlę. Python sam wykona ten kod tyle razy, ile trzeba.

Pętla `for` pobiera kolejne wartości z podanego zakresu. Przy każdej wartości wykonuje instrukcje zapisane we wcięciu.

## Jak czytać pętlę for?

Spójrz na prosty przykład:

```python
for i in range(5):
    print(i)
```

Można to przeczytać tak:

Dla kolejnych wartości zmiennej `i` z zakresu `range(5)` wykonaj instrukcję `print(i)`.

Krok po kroku wygląda to tak:

Najpierw `i` ma wartość `0`.

Potem `i` ma wartość `1`.

Potem `i` ma wartość `2`.

Potem `i` ma wartość `3`.

Potem `i` ma wartość `4`.

Po wartości `4` pętla się kończy.

Ważne: `range(5)` nie oznacza liczb od `1` do `5`, tylko od `0` do `4`.

## Funkcja range()

Funkcja `range()` tworzy zakres liczb, po których może przejść pętla `for`.

`range(5)` daje wartości: `0`, `1`, `2`, `3`, `4`.

`range(1, 6)` daje wartości: `1`, `2`, `3`, `4`, `5`.

`range(2, 11, 2)` daje wartości: `2`, `4`, `6`, `8`, `10`.

W zapisie `range(2, 11, 2)` trzeci argument oznacza krok, czyli o ile zwiększa się wartość zmiennej `i`.

## Liczby od 0 do 4

```python
for i in range(5):
    print(i)
```

Ten kod wypisuje liczby od `0` do `4`.

Omówienie wiersz po wierszu:

Pierwszy wiersz uruchamia pętlę. Zmienna `i` przyjmuje kolejne wartości z `range(5)`.

Drugi wiersz jest wcięty, więc należy do pętli. Wykona się dla każdej wartości `i`.

## Liczby od 1 do 5

```python
for i in range(1, 6):
    print(i)
```

Ten kod wypisuje liczby od `1` do `5`, bo start to `1`, koniec to `6`, a wartość końcowa `6` nie jest już używana.

## Liczby parzyste

```python
for i in range(2, 11, 2):
    print(i)
```

Ten kod wypisuje liczby `2`, `4`, `6`, `8`, `10`.

Trzeci argument, czyli `2`, oznacza krok. Wartość zmiennej `i` zwiększa się za każdym razem o `2`.

## Sumowanie liczb od 1 do n

```python
n = int(input("Podaj n: "))
suma = 0

for i in range(1, n + 1):
    suma = suma + i

print("Suma wynosi:", suma)
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje liczbę `n`.

Drugi wiersz tworzy zmienną `suma`, która zaczyna od `0`.

Pętla przechodzi przez liczby od `1` do `n`.

W każdym obiegu pętla dodaje aktualną wartość `i` do zmiennej `suma`.

Po zakończeniu pętli program wypisuje wynik.

Dla `n = 4` przebieg wygląda tak:

| i | suma przed dodaniem | suma po dodaniu |
|---|----------------------|-----------------|
| 1 | 0 | 1 |
| 2 | 1 | 3 |
| 3 | 3 | 6 |
| 4 | 6 | 10 |

## Iloczyn liczb od 1 do n

```python
n = int(input("Podaj n: "))
iloczyn = 1

for i in range(1, n + 1):
    iloczyn = iloczyn * i

print("Iloczyn wynosi:", iloczyn)
```

Zmienna `iloczyn` zaczyna od `1`, ponieważ mnożenie przez `1` nie zmienia wyniku. Pętla mnoży kolejne liczby od `1` do `n`.

## Tabliczka mnożenia dla jednej liczby

```python
liczba = int(input("Podaj liczbę: "))

for i in range(1, 11):
    wynik = liczba * i
    print(liczba, "*", i, "=", wynik)
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje liczbę od użytkownika.

Pętla przechodzi przez wartości od `1` do `10`.

W każdym obiegu zmienna `wynik` przechowuje wynik mnożenia.

Ostatni wiersz wypisuje jedno działanie z tabliczki mnożenia.

## Typowe błędy uczniów

### Myślenie, że range(5) daje liczby od 1 do 5

`range(5)` daje liczby od `0` do `4`. Jeśli chcesz liczby od `1` do `5`, użyj `range(1, 6)`.

### Brak dwukropka po instrukcji for

```python
for i in range(5)
    print(i)
```

Po instrukcji `for` musi być dwukropek `:`.

### Brak wcięcia instrukcji należących do pętli

```python
for i in range(5):
print(i)
```

Instrukcje należące do pętli muszą być wcięte.

### Mylenie zmiennej sterującej pętli

```python
for i in range(5):
    print(x)
```

W tym przykładzie pętla używa zmiennej `i`, ale program próbuje wypisać `x`. Trzeba pilnować, jak nazywa się zmienna w pętli.

### Wypisanie wyniku w złym miejscu

```python
n = int(input("Podaj n: "))
suma = 0

for i in range(1, n + 1):
    suma = suma + i
    print("Suma wynosi:", suma)
```

Ten kod wypisuje sumę po każdym obiegu pętli. Jeśli chcemy wypisać tylko końcowy wynik, `print()` powinien być bez wcięcia, czyli po pętli.

### Zapomnienie o n + 1

```python
n = int(input("Podaj n: "))

for i in range(1, n):
    print(i)
```

Ten kod nie wypisze liczby `n`. Jeśli chcemy liczyć od `1` do `n`, piszemy `range(1, n + 1)`.

### Używanie for bez sprawdzenia wartości i

Przed napisaniem pętli warto zapytać: jakie wartości będzie miała zmienna `i`? Jeśli to rozumiesz, łatwiej napisać poprawny program.

## Ćwiczenia

1. Wypisz liczby od 0 do 9.
2. Wypisz liczby od 1 do 10.
3. Wypisz liczby od 5 do 15.
4. Wypisz liczby parzyste od 2 do 20.
5. Wczytaj liczbę n i wypisz liczby od 1 do n.
6. Wczytaj liczbę n i oblicz sumę liczb od 1 do n.
7. Wczytaj liczbę n i oblicz iloczyn liczb od 1 do n.
8. Wczytaj liczbę i wypisz jej tabliczkę mnożenia od 1 do 10.
9. Wczytaj liczbę n i wypisz kwadraty liczb od 1 do n.
10. Wczytaj liczbę n i oblicz sumę kwadratów liczb od 1 do n.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
