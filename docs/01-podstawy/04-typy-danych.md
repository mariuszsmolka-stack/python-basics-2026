# Typy danych w Pythonie - int, float, str, bool

## Cel lekcji

Poznasz podstawowe typy danych w Pythonie i nauczysz się sprawdzać typ wartości za pomocą funkcji `type()`.

## Czego się nauczysz

Po tej lekcji będziesz umieć rozpoznawać liczby całkowite, liczby rzeczywiste, teksty i wartości logiczne. Zrozumiesz też, dlaczego `"5"` i `5` to nie to samo.

## Czym jest typ danych

Typ danych mówi Pythonowi, czym jest dana wartość i co można z nią zrobić. Inaczej Python traktuje liczbę, inaczej tekst, a inaczej wartość logiczną `True` albo `False`.

Można to porównać do etykiety. Etykieta mówi, co jest w środku i jak można tego użyć.

## Po co Python rozróżnia typy danych

Python musi wiedzieć, czy ma coś dodać jak liczby, skleić jak teksty, czy sprawdzić jako prawdę albo fałsz.

Dzięki typom danych Python wie, jakie działania są możliwe.

## Liczba i tekst

```python
liczba = 5
tekst = "5"

print(liczba)
print(tekst)
```

Omówienie:

`liczba` przechowuje wartość liczbową `5`.

`tekst` przechowuje znak `"5"` jako tekst.

Dla człowieka wyglądają podobnie.

Dla Pythona to różne typy danych.

## Podstawowe typy danych

`int` to liczba całkowita, na przykład `5`, `-3`, `2026`.

`float` to liczba rzeczywista, na przykład `3.14`, `2.5`, `-7.8`.

`str` to tekst, na przykład `"Anna"`, `"Python"`, `"5"`.

`bool` to wartość logiczna: `True` albo `False`.

```python
wiek = 16
temperatura = 21.5
imie = "Anna"
czy_pelnoletni = False

print(wiek)
print(temperatura)
print(imie)
print(czy_pelnoletni)
```

## Typ int

`int` oznacza liczbę całkowitą.

Liczba całkowita nie ma części po kropce.

```python
rok = 2026
punkty = -3

print(rok)
print(punkty)
```

## Typ float

`float` oznacza liczbę rzeczywistą.

Liczba rzeczywista może mieć część po kropce.

```python
cena = 19.99
temperatura = -7.8

print(cena)
print(temperatura)
```

W Pythonie używamy kropki, na przykład `3.5`, a nie przecinka.

## Typ str

`str` oznacza tekst.

Tekst zapisujemy w cudzysłowie.

```python
imie = "Anna"
napis = "Uczę się Pythona"

print(imie)
print(napis)
```

## Typ bool

`bool` przechowuje jedną z dwóch wartości:

`True`

`False`

```python
wiek = 16
czy_pelnoletni = wiek >= 18

print(czy_pelnoletni)
print(type(czy_pelnoletni))
```

Omówienie:

Wyrażenie `wiek >= 18` daje wynik `True` albo `False`.

W tym przykładzie wynik to `False`.

Takie wartości są używane w instrukcjach `if` i `while`.

## Funkcja type()

Funkcja `type()` pozwala sprawdzić typ wartości albo zmiennej.

```python
wiek = 16
temperatura = 21.5
imie = "Anna"
czy_pelnoletni = False

print(type(wiek))
print(type(temperatura))
print(type(imie))
print(type(czy_pelnoletni))
```

Python wypisze informacje o typach:

`int`

`float`

`str`

`bool`

Funkcja `type()` tylko sprawdza typ. Nie zmienia typu danych.

## "5" i 5 to nie to samo

```python
a = 5
b = "5"

print(a + a)
print(b + b)
```

Omówienie:

`a + a` daje `10`, bo `a` jest liczbą.

`b + b` daje `"55"`, bo `b` jest tekstem.

Znak `+` dla liczb oznacza dodawanie.

Znak `+` dla tekstów oznacza sklejenie tekstów.

## Błąd wynikający z pomylenia tekstu z liczbą

```python
wiek = "16"
za_rok = wiek + 1
print(za_rok)
```

Ten kod spowoduje błąd, ponieważ `wiek` jest tekstem, a `1` jest liczbą.

Jeśli chcemy wykonać obliczenie, potrzebujemy liczby:

```python
wiek = 16
za_rok = wiek + 1
print(za_rok)
```

## input() zawsze zwraca str

```python
liczba = input("Podaj liczbę: ")

print(type(liczba))
```

Omówienie:

Nawet jeśli użytkownik wpisze `10`, `input()` zwróci tekst.

Dlatego typem będzie `str`.

Aby wykonać obliczenia, trzeba użyć `int()` albo `float()`.

Poprawna konwersja:

```python
liczba = int(input("Podaj liczbę: "))
print(type(liczba))
```

## Jak czytać typy danych?

Jeśli wartość jest w cudzysłowie, zwykle jest tekstem.

Jeśli wartość jest liczbą bez kropki, zwykle jest `int`.

Jeśli wartość ma kropkę dziesiętną, zwykle jest `float`.

Jeśli wartość to `True` albo `False`, jest `bool`.

## Typowe błędy uczniów

### Mylenie liczby 5 z tekstem "5"

`5` to liczba.

`"5"` to tekst.

### Dodawanie wartości z input() bez konwersji

```python
a = input("Podaj pierwszą liczbę: ")
b = input("Podaj drugą liczbę: ")
print(a + b)
```

Python sklei teksty. Do obliczeń trzeba użyć `int()` albo `float()`.

### Używanie przecinka zamiast kropki

W Pythonie piszemy `3.5`, a nie `3,5`.

### Zapominanie o cudzysłowie przy tekście

```python
imie = Anna
```

Poprawnie:

```python
imie = "Anna"
```

### Wpisywanie True i False małymi literami

Poprawnie piszemy `True` i `False`.

`true` i `false` nie są tym samym.

### Myślenie, że type() zmienia typ danych

`type()` tylko sprawdza typ. Nie wykonuje konwersji.

### Mylenie str() z tekstem zapisanym w cudzysłowie

`str()` zamienia wartość na tekst.

Tekst zapisany w cudzysłowie już jest tekstem.

### Myślenie, że input() sam rozpoznaje liczby

`input()` zawsze zwraca tekst.

### Próba wykonywania obliczeń na tekście

Do obliczeń potrzebujemy liczb, czyli zwykle `int` albo `float`.

### Nieodróżnianie wartości od jej typu

Wartość to konkretna dana, na przykład `16`.

Typ mówi, czym ta dana jest, na przykład `int`.

## Ćwiczenia

1. Utwórz zmienną z liczbą całkowitą i sprawdź jej typ funkcją type().
2. Utwórz zmienną z liczbą rzeczywistą i sprawdź jej typ.
3. Utwórz zmienną z tekstem i sprawdź jej typ.
4. Utwórz zmienną z wartością True i sprawdź jej typ.
5. Sprawdź, jaki wynik daje 5 + 5 oraz "5" + "5".
6. Wczytaj liczbę za pomocą input() i sprawdź jej typ.
7. Wczytaj liczbę za pomocą input(), zamień ją na int i sprawdź jej typ.
8. Wczytaj cenę jako float i wypisz jej typ.
9. Utwórz zmienną wiek i zmienną czy_pelnoletni z wynikiem porównania wiek >= 18.
10. Napisz krótki program pokazujący różnicę między tekstem "10" i liczbą 10.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
