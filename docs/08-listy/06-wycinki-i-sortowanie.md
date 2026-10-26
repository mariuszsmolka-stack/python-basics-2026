---
layout: default
title: Wycinki i sortowanie
---

# Wycinki i sortowanie

## Cel lekcji

Nauczysz się wybierać fragment listy i porządkować wartości. Rozpoznasz operacje, które zmieniają listę, oraz te, które tworzą nową.

## Czego się nauczysz

- Używać wycinka `lista[start:stop]`.
- Pomijać początek lub koniec wycinka.
- Sortować rosnąco i malejąco.
- Odróżniać `sort()` od `sorted()`.
- Wyjaśniać wynik `None` zwracany przez `sort()`.

## Co to jest wycinek?

Wycinek wybiera fragment listy i tworzy z niego nową listę. W zapisie `lista[start:stop]` początek jest włączony, a koniec jest wyłączony. Wybieramy elementy od indeksu `start` do indeksu tuż przed `stop`.

| Indeks | 0 | 1 | 2 | 3 | 4 |
| --- | --- | --- | --- | --- | --- |
| Wartość | 10 | 20 | 30 | 40 | 50 |
| Czy należy do wycinka `[1:4]`? | nie | tak | tak | tak | nie |

## Pierwszy przykład

```python
liczby = [10, 20, 30, 40, 50]
fragment = liczby[1:4]
print(fragment)
print(liczby)
```

Wynik:

```text
[20, 30, 40]
[10, 20, 30, 40, 50]
```

## Omówienie działania programu

1. Pierwszy wiersz tworzy listę z pięcioma elementami.
2. Indeks `1` wskazuje wartość `20`. Od niej zaczynamy.
3. Indeks `4` wyznacza koniec, którego już nie włączamy. Zatrzymujemy się przed `50`.
4. Zmienna `fragment` wskazuje nową listę z trzema elementami.
5. Lista `liczby` pozostaje bez zmian.

`liczby[1]` dałoby jeden element. `liczby[1:4]` daje listę, nawet gdy wybrany fragment zawiera tylko jeden element albo jest pusty.

## Pomijanie granic

Bez początku wybieramy od pierwszego elementu. Bez końca wybieramy do końca listy. Pominięcie obu granic tworzy kopię całej listy. W tym dziale kopiujemy listy prostych wartości, na przykład liczb lub napisów.

```python
liczby = [10, 20, 30, 40, 50]
print(liczby[:2])
print(liczby[3:])
print(liczby[:])
print(liczby[2:2])
print(liczby[-2:])
```

Wynik:

```text
[10, 20]
[40, 50]
[10, 20, 30, 40, 50]
[]
[40, 50]
```

Wycinek `[2:2]` jest pusty: początek i wyłączony koniec są takie same. Ujemna granica liczy od końca, podobnie jak ujemny indeks. `[-2:]` wybiera dwa ostatnie elementy, jeśli lista ma co najmniej dwa.

Zbyt odległa granica wycinka jest ograniczana do długości listy. Na przykład dla tych danych `liczby[:100]` dałoby całą listę. To inna sytuacja niż odczyt pojedynczego nieistniejącego elementu.

## Sortowanie istniejącej listy: sort()

Sortowanie zmienia kolejność wartości. Domyślny porządek jest rosnący. Metoda `sort()` porządkuje listę, na której została wywołana. Nie usuwa powtórzeń.

```python
liczby = [4, 1, 3, 1]
print(liczby)
liczby.sort()
print(liczby)
```

Wynik:

```text
[4, 1, 3, 1]
[1, 1, 3, 4]
```

Po wywołaniu pierwotna kolejność listy `liczby` jest zmieniona. Jeśli potrzebujesz ją zachować, wybierz `sorted()`.

## Nowa posortowana lista: sorted()

Wbudowana funkcja `sorted(lista)` zwraca nową, posortowaną listę. Nie zmienia przekazanej listy. Zapisujemy wynik w osobnej zmiennej.

```python
liczby = [4, 1, 3]
posortowaneLiczby = sorted(liczby)
print(liczby)
print(posortowaneLiczby)
posortowaneLiczby[0] = 99
print(liczby)
print(posortowaneLiczby)
```

Wynik:

```text
[4, 1, 3]
[1, 3, 4]
[4, 1, 3]
[99, 3, 4]
```

Zmiana pierwszego elementu nowej listy liczb nie zmieniła listy źródłowej. Sam zapis `kopiaLiczb = liczby` nie tworzyłby kopii - obie nazwy wskazywałyby wtedy tę samą listę. Tutaj nową listę utworzyło `sorted()`.

## Sortowanie malejące

Argument `reverse=True` wybiera odwrotny porządek sortowania, czyli dla liczb od największej do najmniejszej. `reverse` jest nazwą argumentu operacji, a `True` to znana wartość logiczna.

```python
liczby = [7, 2, 5]
listaMalejaca = sorted(liczby, reverse=True)
print(listaMalejaca)
print(liczby)
liczby.sort(reverse=True)
print(liczby)
```

Wynik:

```text
[7, 5, 2]
[7, 2, 5]
[7, 5, 2]
```

Pierwsza operacja stworzyła nową listę. Druga zmieniła istniejącą. `reverse=True` nie oznacza jedynie odwrócenia początkowej kolejności. Otrzymujemy wartości uporządkowane malejąco.

## Dlaczego wynikiem sort() jest None?

`None` oznacza tutaj brak zwróconej wartości użytkowej. Metoda wykonała pracę, zmieniając listę. Nie zwraca posortowanej listy tak jak `sorted()`.

```python
liczby = [3, 1, 2]
wynikSortowania = liczby.sort()
print(liczby)
print(wynikSortowania)
```

Wynik:

```text
[1, 2, 3]
None
```

Nie pisz `liczby = liczby.sort()`. Po takim przypisaniu nazwa `liczby` wskazywałaby `None`, a nie listę. Wywołaj `liczby.sort()` osobno i dopiero potem wypisz listę.

| Operacja | Zmienia listę źródłową? | Co zwraca? |
| --- | --- | --- |
| `lista[start:stop]` | nie | nową listę z fragmentem |
| `lista.sort()` | tak | `None` |
| `sorted(lista)` | nie | nową posortowaną listę |

Dla pustej listy wycinki i oba sposoby sortowania są dozwolone. Wynikowa lista pozostaje pusta. Zwracaną wartością `sort()` nadal jest `None`.

## Typowe błędy

- Koniec wycinka nie należy do wyniku.
- Wycinek nie usuwa elementów ze źródła.
- `sort()` nie jest sposobem otrzymania nowej listy w innej zmiennej.
- Wywołanie `sorted(lista)` bez zapisania lub wypisania wyniku nie zmieni źródła.
- Lista liczb i lista napisów to różne dane. Nie próbuj sortować mieszaniny liczb i napisów: Python nie porówna ich w ten sposób.
- Sortowanie napisów nie zawsze odpowiada porządkowi polskiego słownika. Pierwsze ćwiczenia z sortowaniem wykonujemy na liczbach.

## Ćwiczenia

### Ćwiczenie 1. Środek listy

Z listy `liczby = [5, 10, 15, 20, 25]` wybierz elementy z indeksów `1`, `2`, `3` jednym wycinkiem. Wypisz fragment.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Początek jest włączony. Koniec powinien wskazywać pozycję tuż za ostatnim wybranym elementem.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
liczby = [5, 10, 15, 20, 25]
fragment = liczby[1:4]
print(fragment)
```

Wynik:

```text
[10, 15, 20]
```

</details>

### Ćwiczenie 2. Początek i koniec

Dla `oceny = [2, 3, 4, 5, 6]` wypisz pierwsze trzy oceny, a w kolejnym wierszu dwie ostatnie. Użyj wycinków.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

W pierwszym wycinku możesz pominąć początek. W drugim możesz pominąć koniec.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
oceny = [2, 3, 4, 5, 6]
print(oceny[:3])
print(oceny[-2:])
```

Wynik:

```text
[2, 3, 4]
[5, 6]
```

</details>

### Ćwiczenie 3. Zmień kolejność

Posortuj listę `punkty = [9, 2, 7, 2]` rosnąco przez `sort()`. Wypisz zmienioną listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Metoda ma działać na istniejącej liście. Wypisz listę po wykonaniu operacji, a nie wynik zwracany przez metodę.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
punkty = [9, 2, 7, 2]
punkty.sort()
print(punkty)
```

Wynik:

```text
[2, 2, 7, 9]
```

</details>

### Ćwiczenie 4. Zachowaj źródło

Dla `pomiary = [6, 1, 4]` utwórz nową listę rosnącą. Wypisz najpierw listę źródłową, potem nową. Źródło ma zachować kolejność.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Wybierz operację, która zwraca listę, zamiast zmieniać dane wejściowe.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
pomiary = [6, 1, 4]
posortowanePomiary = sorted(pomiary)
print(pomiary)
print(posortowanePomiary)
```

Wynik:

```text
[6, 1, 4]
[1, 4, 6]
```

</details>

### Ćwiczenie 5. Od największej

Utwórz malejącą kopię listy `wyniki = [12, 7, 15, 7]`. Wypisz kopię. Nie zmieniaj listy `wyniki`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Połącz tworzenie nowej listy z argumentem wybierającym malejący porządek.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
wyniki = [12, 7, 15, 7]
wynikiMalejace = sorted(wyniki, reverse=True)
print(wynikiMalejace)
```

Wynik:

```text
[15, 12, 7, 7]
```

</details>

### Ćwiczenie 6. Co zwraca metoda?

Utwórz `liczby = [8, 3, 5]`. Zapisz wynik wywołania `sort()` w zmiennej `wynikMetody`. Wypisz listę i tę zmienną. Wyjaśnij różnicę między ich wartościami.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 6</summary>

Osobno obserwuj skutek działania metody i wartość, którą oddaje wywołanie.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 6</summary>

```python
liczby = [8, 3, 5]
wynikMetody = liczby.sort()
print(liczby)
print(wynikMetody)
```

Wynik:

```text
[3, 5, 8]
None
```

Lista została posortowana. Metoda nie zwróciła posortowanej listy, lecz `None`.

</details>

## Podsumowanie

Wycinek tworzy nową listę i pomija końcowy indeks. `sort()` zmienia istniejącą listę i zwraca `None`. `sorted()` tworzy nową listę, pozostawiając źródło bez zmian.

Jeśli chcesz później zobaczyć, jak można samodzielnie porównywać i przestawiać elementy, zajrzyj do [osobnej lekcji o sortowaniu bąbelkowym](../06-algorytmy/klasa-2/01-sortowanie-babelkowe.md). Ten dodatkowy materiał zawiera też wersje z funkcjami własnymi. Nie jest wymagany do zadań w tym dziale.
