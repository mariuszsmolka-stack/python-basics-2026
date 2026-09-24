# Debugowanie algorytmów

## Cel lekcji

Nauczysz się używać debuggera PyCharm do śledzenia działania algorytmów krok po kroku.

Ta lekcja nie powtarza pełnych lekcji algorytmicznych. Jeśli potrzebujesz wrócić do teorii, skorzystaj z materiałów:

- [Sortowanie bąbelkowe](../06-algorytmy/klasa-2/01-sortowanie-babelkowe.md)
- [NWD i NWW](../06-algorytmy/klasa-3/01-nwd-i-nww.md)

## Sortowanie bąbelkowe

Program do debugowania:

```python
liczby = [4, 2, 5, 1]
liczbaElementow = len(liczby)

for i in range(liczbaElementow - 1):
    for j in range(liczbaElementow - 1):
        if liczby[j] > liczby[j + 1]:
            pomocnicza = liczby[j]
            liczby[j] = liczby[j + 1]
            liczby[j + 1] = pomocnicza

print(liczby)
```

Obserwuj:

- `i`,
- `j`,
- `liczby[j]`,
- `liczby[j + 1]`,
- całą listę `liczby`,
- moment zamiany elementów.

## Praca krok po kroku przy sortowaniu

1. Co chcemy sprawdzić?
   Chcemy zobaczyć, kiedy dwie sąsiednie liczby zamieniają się miejscami.
2. Gdzie zatrzymamy program?
   Ustaw punkt przerwania przy warunku `if liczby[j] > liczby[j + 1]`.
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
   Dla pierwszej pary spodziewamy się porównania `4` i `2`.
4. Wykonujemy jeden krok.
   Sprawdź, czy program wejdzie do instrukcji `if`.
5. Porównujemy przewidywanie z rzeczywistą wartością.
   Ponieważ `4 > 2`, powinna nastąpić zamiana.
6. Wyciągamy wniosek.
   Debugger pokazuje dokładny moment zamiany elementów listy.

## Tabela stanów sortowania

| Krok | `i` | `j` | `liczby[j]` | `liczby[j + 1]` | Lista przed krokiem | Lista po kroku |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| 1 | 0 | 0 | 4 | 2 | `[4, 2, 5, 1]` | `[2, 4, 5, 1]` |
| 2 | 0 | 1 | 4 | 5 | `[2, 4, 5, 1]` | `[2, 4, 5, 1]` |
| 3 | 0 | 2 | 5 | 1 | `[2, 4, 5, 1]` | `[2, 4, 1, 5]` |

## Algorytm Euklidesa

Program do debugowania:

```python
a = 18
b = 24

while b != 0:
    reszta = a % b
    a = b
    b = reszta

print("NWD:", a)
```

Obserwuj:

- `a`,
- `b`,
- `reszta`.

## Praca krok po kroku przy NWD

1. Co chcemy sprawdzić?
   Chcemy zobaczyć, jak zmieniają się `a`, `b` i `reszta`.
2. Gdzie zatrzymamy program?
   Ustaw punkt przerwania przy wierszu `reszta = a % b`.
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
   Dla `a = 18` i `b = 24` spodziewamy się reszty `18`.
4. Wykonujemy jeden krok.
   Wykonaj obliczenie reszty.
5. Porównujemy przewidywanie z rzeczywistą wartością.
   Sprawdź wartość `reszta` w panelu `Variables`.
6. Wyciągamy wniosek.
   Algorytm stopniowo zmniejsza liczby, aż `b` będzie równe `0`.

## Tabela stanów NWD

| Krok | `a` przed | `b` przed | `reszta` | `a` po | `b` po |
| --- | ---: | ---: | ---: | ---: | ---: |
| 1 | 18 | 24 | 18 | 24 | 18 |
| 2 | 24 | 18 | 6 | 18 | 6 |
| 3 | 18 | 6 | 0 | 6 | 0 |

## Ćwiczenia

1. Prześledź sortowanie listy `[3, 1, 2]`.
2. Przy każdej zamianie zapisz stan całej listy.
3. Dodaj do `Watches` wyrażenia `liczby[j]` i `liczby[j + 1]`.
4. Sprawdź, przy których wartościach `i` i `j` następuje zamiana.
5. Prześledź algorytm Euklidesa dla liczb `12` i `18`.
6. Przed każdym krokiem przewiduj wartość `reszta`.
7. Uzupełnij tabelę stanów NWD dla liczb `20` i `30`.
8. Wyjaśnij własnymi słowami, jak debugger pomaga zrozumieć algorytm.
