# Warunki i pętle

## Cel lekcji

Nauczysz się sprawdzać w debuggerze działanie warunków `if` oraz pętli.

## Debugowanie prostego warunku

Program:

```python
liczba = 12

if liczba > 10:
    print("Liczba jest większa od 10")
else:
    print("Liczba nie jest większa od 10")
```

Przed wejściem do warunku przewidujemy, która gałąź programu zostanie wykonana. Potem wykonujemy krok i sprawdzamy, czy PyCharm przechodzi do oczekiwanego wiersza.

## Pętla i akumulator

Program do ćwiczenia:

```python
suma = 0

for liczba in range(1, 6):
    suma = suma + liczba

print(suma)
```

Obserwujemy:

- `liczba`,
- `suma`.

## Praca krok po kroku

1. Co chcemy sprawdzić?
   Chcemy sprawdzić kolejne wartości licznika `liczba` i akumulatora `suma`.
2. Gdzie zatrzymamy program?
   Ustaw punkt przerwania przy wierszu `suma = suma + liczba`.
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
   W pierwszym obiegu `liczba` powinna mieć wartość `1`, a `suma` wartość `0`.
4. Wykonujemy jeden krok.
   Naciśnij `F8`.
5. Porównujemy przewidywanie z rzeczywistą wartością.
   Po pierwszym dodaniu `suma` powinna mieć wartość `1`.
6. Wyciągamy wniosek.
   Każdy obieg pętli zmienia wartość akumulatora.

## Tabela obiegów pętli

| Obieg | `liczba` przed dodaniem | `suma` przed dodaniem | `suma` po dodaniu |
| --- | ---: | ---: | ---: |
| 1 | 1 | 0 | 1 |
| 2 | 2 | 1 | 3 |
| 3 | 3 | 3 | 6 |
| 4 | 4 | 6 | 10 |
| 5 | 5 | 10 | 15 |

## Gdy pętla nie wykona się ani razu

Program:

```python
suma = 0

for liczba in range(1, 1):
    suma = suma + liczba

print(suma)
```

Zakres `range(1, 1)` nie daje żadnej liczby. Pętla nie wykonuje się ani razu. Debugger pomaga to zauważyć, bo program od razu przechodzi do `print(suma)`.

## Błąd o jeden

Program z błędem:

```python
suma = 0

for liczba in range(1, 5):
    suma = suma + liczba

print(suma)
```

Ten program miał obliczyć sumę liczb od `1` do `5`, ale wynik będzie za mały.

<details markdown="1">
<summary>Pokaż wyjaśnienie i poprawione rozwiązanie</summary>

W `range(1, 5)` liczba `5` nie jest używana. Zakres daje wartości `1`, `2`, `3`, `4`.

Poprawiony kod:

```python
suma = 0

for liczba in range(1, 6):
    suma = suma + liczba

print(suma)
```

</details>

## Ćwiczenia

1. Sprawdź w debuggerze, która gałąź instrukcji `if` zostanie wykonana.
2. Zmień `liczba = 12` na `liczba = 8` i powtórz debugowanie.
3. W programie z pętlą obserwuj zmienne `liczba` i `suma`.
4. Uzupełnij tabelę obiegów pętli.
5. Sprawdź, ile razy wykona się pętla `range(1, 6)`.
6. Uruchom program z `range(1, 1)` i zobacz, że pętla się nie wykona.
7. Znajdź błąd w programie z `range(1, 5)`.
8. Napisz podobny program sumujący liczby od `1` do `10` i sprawdź go debuggerem.
