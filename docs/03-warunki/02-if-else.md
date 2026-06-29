# Instrukcja warunkowa if-else w Pythonie

## Cel lekcji

Poznasz instrukcję `if-else` i nauczysz się wybierać jedną z dwóch możliwości w programie.

## Czego się nauczysz

Po tej lekcji będziesz umieć zapisać warunek z dwiema odpowiedziami. Dowiesz się, kiedy wykona się część `if`, kiedy wykona się część `else` oraz jak poprawnie używać dwukropków i wcięć.

## Przypomnienie instrukcji if

Instrukcja `if` pozwala wykonać kod tylko wtedy, gdy warunek jest prawdziwy.

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
```

Jeśli warunek `liczba > 0` jest prawdziwy, program wyświetli komunikat. Jeśli warunek jest fałszywy, program nic nie wypisze w tej części.

## Po co używamy else

`else` używamy wtedy, gdy chcemy powiedzieć programowi, co ma zrobić w przeciwnym przypadku.

Część `else` wykonuje się wtedy, gdy warunek w `if` nie jest spełniony.

`else` nie ma własnego warunku. Oznacza po prostu: w przeciwnym razie.

## Składnia if-else

Podstawowy zapis wygląda tak:

```python
if warunek:
    instrukcje_gdy_prawda
else:
    instrukcje_gdy_fałsz
```

Część `if` sprawdza warunek.

Kod pod `if` wykona się, gdy warunek jest prawdziwy.

Kod pod `else` wykona się, gdy warunek jest fałszywy.

`else` nie ma własnego warunku.

Po `else` też stawiamy dwukropek `:`.

Instrukcje należące do `if` i `else` muszą być wcięte.

## Jak czytać if-else?

Instrukcję `if-else` można czytać tak:

Jeśli warunek jest prawdziwy, wykonaj pierwszą część. W przeciwnym razie wykonaj drugą część.

W jednej instrukcji `if-else` wykona się tylko jedna część: albo część pod `if`, albo część pod `else`.

## Liczba dodatnia albo niedodatnia

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
else:
    print("Liczba nie jest dodatnia.")
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje liczbę od użytkownika i zamienia ją na liczbę całkowitą.

Wiersz z `if` sprawdza, czy `liczba > 0`.

Jeśli warunek jest prawdziwy, program wypisuje `Liczba jest dodatnia.`.

Jeśli warunek jest fałszywy, program przechodzi do `else`.

Część `else` wypisuje `Liczba nie jest dodatnia.`.

## Sprawdzanie pełnoletności

```python
wiek = int(input("Podaj swój wiek: "))

if wiek >= 18:
    print("Jesteś osobą pełnoletnią.")
else:
    print("Nie jesteś jeszcze osobą pełnoletnią.")
```

Program sprawdza, czy wiek jest większy lub równy `18`. Jeśli tak, wyświetla pierwszy komunikat. W przeciwnym razie wyświetla drugi komunikat.

## Sprawdzanie hasła

```python
haslo = input("Podaj hasło: ")

if haslo == "python":
    print("Hasło poprawne.")
else:
    print("Hasło niepoprawne.")
```

Operator `==` sprawdza, czy wpisany tekst jest równy `"python"`. Jeśli hasło jest poprawne, wykona się część `if`. Jeśli hasło jest inne, wykona się część `else`.

## Liczba parzysta albo nieparzysta

```python
liczba = int(input("Podaj liczbę: "))

if liczba % 2 == 0:
    print("Liczba jest parzysta.")
else:
    print("Liczba jest nieparzysta.")
```

Operator `%` zwraca resztę z dzielenia. Liczba parzysta daje resztę `0` przy dzieleniu przez `2`.

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje liczbę całkowitą.

Warunek `liczba % 2 == 0` sprawdza, czy reszta z dzielenia przez `2` wynosi `0`.

Jeśli warunek jest prawdziwy, liczba jest parzysta.

Jeśli warunek jest fałszywy, liczba jest nieparzysta.

## Przykład z temperaturą

```python
temperatura = float(input("Podaj temperaturę: "))

if temperatura > 30:
    print("Jest bardzo gorąco.")
else:
    print("Temperatura nie przekracza 30 stopni.")
```

Program wczytuje temperaturę jako liczbę rzeczywistą. Jeśli temperatura jest większa niż `30`, pojawia się pierwszy komunikat. W przeciwnym razie pojawia się drugi komunikat.

## Typowe błędy uczniów

### Brak dwukropka po if

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0
    print("Liczba jest dodatnia.")
else:
    print("Liczba nie jest dodatnia.")
```

Po warunku w `if` musi być dwukropek `:`.

### Brak dwukropka po else

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
else
    print("Liczba nie jest dodatnia.")
```

Po `else` też musi być dwukropek `:`.

### Dopisywanie warunku po else

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
else liczba > 0:
    print("Liczba nie jest dodatnia.")
```

`else` nie ma własnego warunku. Oznacza przeciwny przypadek.

### Brak wcięć

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
print("Liczba jest dodatnia.")
else:
print("Liczba nie jest dodatnia.")
```

Instrukcje należące do `if` i `else` muszą być wcięte.

### Mylenie = oraz ==

```python
haslo = input("Podaj hasło: ")

if haslo = "python":
    print("Hasło poprawne.")
else:
    print("Hasło niepoprawne.")
```

Znak `=` służy do przypisania wartości. Do porównania używamy `==`.

### Myślenie, że wykona się jednocześnie if i else

W instrukcji `if-else` wykona się tylko jedna część. Jeśli warunek jest prawdziwy, wykona się `if`. Jeśli warunek jest fałszywy, wykona się `else`.

### Złe miejsce instrukcji print()

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
else:
    print("Liczba nie jest dodatnia.")
print("Koniec programu.")
```

Ostatni `print()` nie jest wcięty, więc nie należy ani do `if`, ani do `else`. Wykona się zawsze.

## Ćwiczenia

1. Wczytaj liczbę i sprawdź, czy jest dodatnia, czy niedodatnia.
2. Wczytaj wiek i sprawdź, czy użytkownik jest pełnoletni.
3. Wczytaj hasło i sprawdź, czy jest poprawne.
4. Wczytaj liczbę i sprawdź, czy jest parzysta, czy nieparzysta.
5. Wczytaj temperaturę i sprawdź, czy jest większa od 30.
6. Wczytaj liczbę punktów i sprawdź, czy uczeń zaliczył test. Za zaliczenie przyjmij co najmniej 50 punktów.
7. Wczytaj cenę produktu i sprawdź, czy jest większa niż 100.
8. Wczytaj liczbę i sprawdź, czy jest równa 0.
9. Wczytaj imię i sprawdź, czy użytkownik coś wpisał.
10. Wczytaj wzrost w centymetrach i sprawdź, czy jest większy niż 180.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
