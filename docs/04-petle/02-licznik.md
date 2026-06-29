# Licznik, akumulator i skrócone operatory przypisania w Pythonie

## Cel lekcji

Poznasz licznik, akumulator oraz skrócone operatory przypisania. Nauczysz się używać ich w prostych pętlach.

## Czego się nauczysz

Po tej lekcji będziesz umieć zwiększać licznik, gromadzić wynik w akumulatorze oraz zapisywać prościej działania typu `licznik = licznik + 1`.

## Czym jest licznik

Licznik to zmienna, która liczy, ile razy coś się wydarzyło.

Licznik działa jak kreski stawiane na kartce. Za każdym razem, gdy coś się wydarzy, dopisujemy jedną kreskę. W programie zamiast kreski zwiększamy zmienną o `1`.

Najczęściej licznik zaczyna od `0` albo od `1`.

## Zwiększanie licznika o 1

```python
licznik = licznik + 1
```

Ten zapis oznacza: weź starą wartość zmiennej `licznik`, dodaj `1` i zapisz wynik z powrotem do tej samej zmiennej.

Ten sam zapis można skrócić:

```python
licznik += 1
```

Oba zapisy znaczą to samo.

## Przykład licznika

```python
licznik = 0

while licznik < 5:
    licznik += 1
    print("Obieg pętli numer:", licznik)
```

Omówienie wiersz po wierszu:

`licznik` zaczyna od `0`.

Pętla działa dopóki `licznik` jest mniejszy od `5`.

W każdym obiegu `licznik` zwiększa się o `1`.

Program wypisuje numer obiegu.

Po osiągnięciu `5` pętla się kończy.

## Czym jest akumulator

Akumulator to zmienna, w której stopniowo gromadzimy wynik.

Najczęściej akumulator przechowuje sumę, iloczyn albo inny wynik obliczany krok po kroku.

Przykład: jeśli dodajemy wiele liczb, akumulatorem może być zmienna `suma`.

## Różnica między licznikiem i akumulatorem

Licznik zwykle odpowiada na pytanie: ile razy?

Akumulator zwykle odpowiada na pytanie: jaki wynik się zgromadził?

Licznik często zwiększamy o `1`.

Akumulator często zwiększamy o wartość innej zmiennej.

## Sumowanie liczb

```python
i = 1
suma = 0

while i <= 5:
    suma += i
    i += 1

print(suma)
```

W tym przykładzie `i` jest licznikiem, a `suma` jest akumulatorem.

Zapis `suma += i` oznacza to samo co:

```python
suma = suma + i
```

Najpierw trzeba rozumieć zapis pełny:

```python
suma = suma + i
```

Dopiero potem wygodnie używać zapisu skróconego:

```python
suma += i
```

## Suma liczb od 1 do n

```python
n = int(input("Podaj n: "))
i = 1
suma = 0

while i <= n:
    suma += i
    i += 1

print("Suma wynosi:", suma)
```

Omówienie:

`i` jest licznikiem.

`suma` jest akumulatorem.

`i` przechodzi przez kolejne liczby.

`suma` gromadzi wynik.

Zapis `suma += i` oznacza to samo co `suma = suma + i`.

Dla `n = 4` przebieg wygląda tak:

| i | suma przed dodaniem | suma po dodaniu |
|---|----------------------|-----------------|
| 1 | 0 | 1 |
| 2 | 1 | 3 |
| 3 | 3 | 6 |
| 4 | 6 | 10 |

## Liczenie iloczynu liczb

```python
n = int(input("Podaj n: "))
i = 1
iloczyn = 1

while i <= n:
    iloczyn *= i
    i += 1

print("Iloczyn wynosi:", iloczyn)
```

Dla mnożenia akumulator zwykle zaczyna od `1`, a nie od `0`, bo mnożenie przez `0` wyzerowałoby wynik.

W tym przykładzie `iloczyn *= i` oznacza to samo co:

```python
iloczyn = iloczyn * i
```

## Zliczanie obiegów pętli

```python
obieg = 0
liczba = 100

while liczba > 0:
    obieg += 1
    liczba -= 20

print("Liczba obiegów:", obieg)
```

Zmienna `obieg` liczy, ile razy wykonała się pętla. Zmienna `liczba` zmienia się tak, aby pętla mogła się zakończyć.

## Licznik czy akumulator?

```python
i = 1
suma = 0

while i <= 5:
    suma += i
    i += 1

print(suma)
```

W tym kodzie `i` jest licznikiem, bo przechodzi przez kolejne wartości.

`suma` jest akumulatorem, bo gromadzi wynik dodawania.

## Skrócone operatory przypisania

Skrócone operatory przypisania pozwalają zapisać krócej częste działania na tej samej zmiennej.

`x += 1` oznacza `x = x + 1`.

`x -= 1` oznacza `x = x - 1`.

`x *= 2` oznacza `x = x * 2`.

`x /= 2` oznacza `x = x / 2`.

`x //= 2` oznacza `x = x // 2`.

`x %= 2` oznacza `x = x % 2`.

| Zapis skrócony | Zapis pełny | Znaczenie |
|----------------|-------------|-----------|
| x += 1 | x = x + 1 | zwiększ x o 1 |
| x -= 1 | x = x - 1 | zmniejsz x o 1 |
| x *= 2 | x = x * 2 | pomnóż x przez 2 |
| x /= 2 | x = x / 2 | podziel x przez 2 |
| x //= 2 | x = x // 2 | podziel całkowicie x przez 2 |
| x %= 2 | x = x % 2 | zapisz resztę z dzielenia przez 2 |

## Porównanie zapisu pełnego i skróconego

```python
licznik = 0
licznik = licznik + 1
print(licznik)
```

Ten kod można zapisać krócej:

```python
licznik = 0
licznik += 1
print(licznik)
```

Oba programy wypiszą ten sam wynik.

## Jak czytać taki kod?

Przykład:

```python
suma += liczba
```

Można to przeczytać tak: do obecnej sumy dodaj wartość zmiennej `liczba`.

Przykład:

```python
i += 1
```

Można to przeczytać tak: zwiększ licznik `i` o `1`.

## Typowe błędy uczniów

### Brak wartości początkowej licznika

Przed pętlą trzeba ustawić początkową wartość licznika.

```python
i = 1
```

### Brak wartości początkowej akumulatora

Akumulator też musi mieć wartość początkową.

```python
suma = 0
```

### Ustawienie iloczynu początkowo na 0

Przy mnożeniu akumulator zaczyna zwykle od `1`.

```python
iloczyn = 1
```

Jeśli zacznie od `0`, wynik mnożenia będzie cały czas równy `0`.

### Zapomnienie o zwiększaniu licznika w pętli while

```python
i = 1

while i <= 5:
    print(i)
```

Ten program może działać bez końca, bo `i` się nie zmienia.

### Mylenie licznika z akumulatorem

Licznik zwykle liczy kroki. Akumulator gromadzi wynik.

### Wypisywanie wyniku końcowego wewnątrz pętli

```python
n = int(input("Podaj n: "))
i = 1
suma = 0

while i <= n:
    suma += i
    i += 1
    print("Suma wynosi:", suma)
```

Ten kod wypisuje sumę po każdym obiegu. Wynik końcowy powinien być wypisany po pętli, bez wcięcia.

### Myślenie, że suma += i tworzy nową zmienną

Zapis `suma += i` nie tworzy nowej zmiennej. On zmienia starą wartość zmiennej `suma`.

### Mylenie += z =+

Poprawny zapis to:

```python
suma += i
```

Zapis `=+` nie oznacza dodawania do starej wartości.

### Używanie skróconego operatora bez rozumienia zapisu pełnego

Najpierw przeczytaj zapis pełny:

```python
suma = suma + i
```

Potem użyj zapisu skróconego:

```python
suma += i
```

### Zmiana złej zmiennej

```python
suma += 1
```

Ten zapis zwiększa sumę o `1`. Jeśli chcemy dodać aktualną wartość licznika, trzeba napisać:

```python
suma += i
```

## Ćwiczenia

1. Utwórz licznik, który wypisze liczby od 1 do 5.
2. Wczytaj n i wypisz liczby od 1 do n.
3. Wczytaj n i oblicz sumę liczb od 1 do n.
4. Wczytaj n i oblicz iloczyn liczb od 1 do n.
5. Wczytaj n i oblicz sumę liczb parzystych od 2 do n.
6. Wczytaj n i oblicz sumę kwadratów liczb od 1 do n.
7. Wczytaj n i policz, ile razy wykonała się pętla.
8. Wczytaj cenę produktu i liczbę sztuk, a następnie oblicz łączny koszt, dodając cenę produktu kilka razy w pętli.
9. Napisz program, który zaczyna od liczby 100 i zmniejsza ją o 10, dopóki jest większa od 0.
10. Napisz program, który zaczyna od liczby 1 i w każdym kroku mnoży ją przez 2, aż wykona 8 kroków.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
