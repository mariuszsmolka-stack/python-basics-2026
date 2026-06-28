# Operatory w Pythonie

## Cel lekcji

Poznasz podstawowe operatory w Pythonie i zobaczysz, jak używać ich w prostych programach.

## Czego się nauczysz

Nauczysz się wykonywać podstawowe działania matematyczne, porównywać wartości oraz łączyć proste warunki logiczne. Zobaczysz też, jak operatory mogą pomagać w podejmowaniu decyzji w programie.

## Czym są operatory

Operatory to znaki lub słowa, które wykonują działanie na danych. Mogą służyć do liczenia, porównywania wartości albo sprawdzania kilku warunków naraz.

Przykładem operatora jest znak `+`, który dodaje liczby, albo znak `>`, który sprawdza, czy jedna wartość jest większa od drugiej.

## Operatory arytmetyczne

Operatory arytmetyczne służą do wykonywania działań na liczbach.

`+` dodaje wartości.

`-` odejmuje wartości.

`*` mnoży wartości.

`/` dzieli wartości i zwraca wynik z częścią dziesiętną.

`//` wykonuje dzielenie całkowite.

`%` zwraca resztę z dzielenia.

`**` oznacza potęgowanie.

### Przykład

```python
a = 10
b = 3

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a // b)
print(a % b)
print(a ** b)
```

W tym przykładzie zmienne `a` i `b` przechowują liczby. Każda instrukcja `print()` pokazuje wynik innego działania arytmetycznego.

## Operatory porównania

Operatory porównania służą do sprawdzania relacji między wartościami. Wynikiem porównania jest wartość `True` albo `False`.

`==` sprawdza, czy wartości są równe.

`!=` sprawdza, czy wartości są różne.

`>` sprawdza, czy pierwsza wartość jest większa.

`<` sprawdza, czy pierwsza wartość jest mniejsza.

`>=` sprawdza, czy pierwsza wartość jest większa lub równa.

`<=` sprawdza, czy pierwsza wartość jest mniejsza lub równa.

### Przykład

```python
wiek = 15

print(wiek == 15)
print(wiek != 18)
print(wiek > 13)
print(wiek < 18)
print(wiek >= 15)
print(wiek <= 16)
```

W tym przykładzie program porównuje wartość zmiennej `wiek` z innymi liczbami. Każde porównanie daje wynik `True` lub `False`.

### Przykład z instrukcją if

```python
ocena = 5

if ocena >= 2:
    print("Ocena jest pozytywna")
```

W tym przykładzie program sprawdza, czy ocena jest większa lub równa `2`. Jeśli warunek jest prawdziwy, wyświetla komunikat.

## Operatory logiczne

Operatory logiczne służą do łączenia warunków.

`and` oznacza, że oba warunki muszą być prawdziwe.

`or` oznacza, że wystarczy jeden prawdziwy warunek.

`not` odwraca wynik warunku.

### Przykład z operatorem and

```python
wiek = 15
zgoda_rodzica = True

if wiek >= 13 and zgoda_rodzica == True:
    print("Możesz wziąć udział w zajęciach")
```

W tym przykładzie oba warunki muszą być spełnione. Uczeń musi mieć co najmniej 13 lat i musi mieć zgodę rodzica.

### Przykład z operatorem or

```python
ma_legitymacje = True
ma_bilet = False

if ma_legitymacje == True or ma_bilet == True:
    print("Możesz wejść")
```

W tym przykładzie wystarczy spełnić jeden warunek. Program wyświetli komunikat, jeśli osoba ma legitymację albo bilet.

### Przykład z operatorem not

```python
jest_zalogowany = False

if not jest_zalogowany:
    print("Zaloguj się")
```

W tym przykładzie operator `not` odwraca wartość warunku. Ponieważ zmienna `jest_zalogowany` ma wartość `False`, program wyświetla komunikat.

## Ćwiczenia

### Ćwiczenie 1

Utwórz dwie zmienne z liczbami. Wyświetl wynik dodawania, odejmowania, mnożenia i dzielenia tych liczb.

### Ćwiczenie 2

Utwórz zmienną `wiek`. Sprawdź za pomocą operatorów porównania, czy osoba ma co najmniej 18 lat.

### Ćwiczenie 3

Utwórz zmienne `temperatura` i `pada_deszcz`. Napisz prostą instrukcję `if`, która wyświetli komunikat, gdy temperatura jest większa niż 20 i nie pada deszcz.

### Ćwiczenie 4

Utwórz zmienną `liczba`. Sprawdź, czy reszta z dzielenia tej liczby przez `2` wynosi `0`.

## Sposób oddania pracy

Wykonaj ćwiczenia w JupyterLab. Gotowe rozwiązania zapisz w swoim folderze w JupyterLab.
