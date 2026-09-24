# Ćwiczenia podsumowujące

## Cel lekcji

Utrwalisz pracę z debuggerem PyCharm na krótkich programach w plikach `.py`.

## Punkty przerwania

### Ćwiczenie 1

Utwórz program:

```python
cena = 8
liczbaSztuk = 4
koszt = cena * liczbaSztuk
print(koszt)
```

Ustaw punkt przerwania przy obliczaniu `koszt`. Przewidź wartość, wykonaj krok i sprawdź wynik.

### Ćwiczenie 2

Ustaw punkt przerwania przy ostatnim wierszu programu i sprawdź, które zmienne już istnieją.

## Wykonywanie krok po kroku

### Ćwiczenie 3

Prześledź program:

```python
wynik = 5
wynik = wynik + 10
wynik = wynik * 3
print(wynik)
```

Przed każdym krokiem zapisz przewidywaną wartość `wynik`.

### Ćwiczenie 4

Uruchom program ponownie i użyj `Resume Program` (`F9`) po pierwszym zatrzymaniu.

## Podgląd zmiennych

### Ćwiczenie 5

Prześledź program:

```python
liczby = [2, 4, 6]
suma = 0
suma = suma + liczby[0]
suma = suma + liczby[1]
suma = suma + liczby[2]
print(suma)
```

Obserwuj `liczby`, `suma` oraz `len(liczby)`.

## Warunki

### Ćwiczenie 6

Znajdź błąd logiczny:

```python
punkty = 45

if punkty > 50:
    print("Zaliczone")
else:
    print("Brak zaliczenia")
```

Program miał zaliczać wynik od `50` punktów włącznie. Nie zaznaczaj od razu miejsca błędu. Użyj debuggera i sprawdź warunek.

<details markdown="1">
<summary>Pokaż wyjaśnienie błędu i poprawkę</summary>

Błąd polega na użyciu warunku `punkty > 50`. Dla dokładnie `50` punktów warunek będzie fałszywy.

Poprawiony kod:

```python
punkty = 45

if punkty >= 50:
    print("Zaliczone")
else:
    print("Brak zaliczenia")
```

</details>

### Ćwiczenie 7

Znajdź pomyloną zmienną w warunku:

```python
wiek = 16
limit = 18

if limit >= 18:
    print("Pełnoletni")
else:
    print("Niepełnoletni")
```

<details markdown="1">
<summary>Pokaż wyjaśnienie błędu i poprawkę</summary>

Warunek sprawdza `limit`, a powinien sprawdzać `wiek`.

Poprawiony kod:

```python
wiek = 16
limit = 18

if wiek >= limit:
    print("Pełnoletni")
else:
    print("Niepełnoletni")
```

</details>

## Pętle

### Ćwiczenie 8

Znajdź błąd w akumulatorze:

```python
suma = 1

for liczba in range(1, 6):
    suma = suma + liczba

print(suma)
```

Program miał obliczyć sumę liczb od `1` do `5`.

<details markdown="1">
<summary>Pokaż wyjaśnienie błędu i poprawkę</summary>

Akumulator `suma` powinien zaczynać od `0`, a nie od `1`.

Poprawiony kod:

```python
suma = 0

for liczba in range(1, 6):
    suma = suma + liczba

print(suma)
```

</details>

### Ćwiczenie 9

Znajdź błąd w zakresie:

```python
iloczyn = 1

for liczba in range(1, 5):
    iloczyn = iloczyn * liczba

print(iloczyn)
```

Program miał obliczyć iloczyn liczb od `1` do `5`.

<details markdown="1">
<summary>Pokaż wyjaśnienie błędu i poprawkę</summary>

`range(1, 5)` kończy się na liczbie `4`. Aby użyć liczby `5`, trzeba zapisać `range(1, 6)`.

Poprawiony kod:

```python
iloczyn = 1

for liczba in range(1, 6):
    iloczyn = iloczyn * liczba

print(iloczyn)
```

</details>

## Funkcje

### Ćwiczenie 10

Prześledź funkcję za pomocą `Step Into` (`F7`):

```python
def obliczKoszt(cena, liczbaSztuk):
    koszt = cena * liczbaSztuk
    return koszt


wynik = obliczKoszt(7, 3)
print(wynik)
```

### Ćwiczenie 11

Znajdź błędną wartość zwracaną przez funkcję:

```python
def obliczPoleProstokata(dlugosc, szerokosc):
    pole = dlugosc * szerokosc
    obwod = 2 * dlugosc + 2 * szerokosc
    return obwod


wynik = obliczPoleProstokata(5, 3)
print(wynik)
```

Funkcja miała zwracać pole prostokąta.

<details markdown="1">
<summary>Pokaż wyjaśnienie błędu i poprawkę</summary>

Funkcja oblicza `pole`, ale zwraca `obwod`.

Poprawiony kod:

```python
def obliczPoleProstokata(dlugosc, szerokosc):
    pole = dlugosc * szerokosc
    return pole


wynik = obliczPoleProstokata(5, 3)
print(wynik)
```

</details>

### Ćwiczenie 12

Znajdź nieprawidłową kolejność obliczeń:

```python
def obliczCeneBrutto(cenaNetto):
    cenaBrutto = cenaNetto + 23
    return cenaBrutto


wynik = obliczCeneBrutto(100)
print(wynik)
```

Program miał doliczyć `23%` podatku, a nie `23` zł.

<details markdown="1">
<summary>Pokaż wyjaśnienie błędu i poprawkę</summary>

Błąd polega na dodaniu liczby `23` zamiast pomnożenia ceny netto przez `1.23`.

Poprawiony kod:

```python
def obliczCeneBrutto(cenaNetto):
    cenaBrutto = cenaNetto * 1.23
    return cenaBrutto


wynik = obliczCeneBrutto(100)
print(wynik)
```

</details>

## Listy i algorytmy

### Ćwiczenie 13

Prześledź fragment sortowania:

```python
liczby = [3, 1, 2]

if liczby[0] > liczby[1]:
    pomocnicza = liczby[0]
    liczby[0] = liczby[1]
    liczby[1] = pomocnicza

print(liczby)
```

Obserwuj całą listę `liczby`.

### Ćwiczenie 14

Prześledź algorytm Euklidesa:

```python
a = 20
b = 12

while b != 0:
    reszta = a % b
    a = b
    b = reszta

print(a)
```

Przed każdym krokiem przewiduj wartość `reszta`.

### Ćwiczenie 15

Znajdź błąd logiczny:

```python
liczby = [4, 2, 1]

if liczby[0] < liczby[1]:
    pomocnicza = liczby[0]
    liczby[0] = liczby[1]
    liczby[1] = pomocnicza

print(liczby)
```

Program miał zamienić pierwsze dwa elementy, jeśli są w złej kolejności rosnącej.

<details markdown="1">
<summary>Pokaż wyjaśnienie błędu i poprawkę</summary>

Dla sortowania rosnącego zamieniamy elementy wtedy, gdy lewy element jest większy od prawego.

Poprawiony kod:

```python
liczby = [4, 2, 1]

if liczby[0] > liczby[1]:
    pomocnicza = liczby[0]
    liczby[0] = liczby[1]
    liczby[1] = pomocnicza

print(liczby)
```

</details>

### Ćwiczenie 16

Wybierz jeden program z tej lekcji i opisz własnymi słowami:

1. gdzie ustawiasz punkt przerwania,
2. jaką wartość przewidujesz,
3. jaki wynik pokazał debugger,
4. jaki wniosek z tego wynika.
