# Funkcja print() w Pythonie - wypisywanie tekstu i wartości

## Cel lekcji

Poznasz funkcję `print()` i nauczysz się wypisywać na ekranie tekst, liczby, wyniki obliczeń oraz wartości zmiennych.

## Czego się nauczysz

Po tej lekcji będziesz umieć używać `print()` do pokazywania informacji użytkownikowi. Nauczysz się też używać przecinków w `print()` oraz poznasz f-stringi jako dodatek dla chętnych.

## Czym jest print()

Funkcja `print()` służy do wypisywania informacji na ekranie. Dzięki niej program może pokazać użytkownikowi tekst, liczbę, wynik obliczenia albo wartość zmiennej.

Można o niej myśleć tak: `print()` to sposób, w jaki program mówi coś do użytkownika.

## Wypisanie prostego tekstu

```python
print("Cześć!")
```

Omówienie:

`print` oznacza: wypisz na ekranie.

Tekst umieszczamy w cudzysłowie.

Python wypisze: `Cześć!`

## Wypisanie liczby

```python
print(2026)
```

Liczby nie muszą być zapisane w cudzysłowie.

Python wypisze liczbę `2026`.

## Wypisanie kilku tekstów

```python
print("Uczę się", "Pythona")
```

Funkcja `print()` może wypisać kilka elementów w jednym wierszu.

Przecinek oddziela elementy, które chcemy wypisać.

## Wypisanie tekstu i liczby

```python
print("Rok:", 2026)
```

Pierwszy element to tekst `"Rok:"`.

Drugi element to liczba `2026`.

Python wypisze oba elementy w jednym wierszu.

## Wypisanie wartości zmiennej

```python
imie = "Anna"
print("Cześć,", imie)
```

Omówienie:

`"Cześć,"` to tekst.

`imie` to zmienna.

Przecinek oddziela tekst od zmiennej.

Python wypisze oba elementy w jednym wierszu.

Python automatycznie doda odstęp między elementami.

## Przecinki w funkcji print()

W podstawowej wersji funkcji `print()` przecinki są bardzo ważne. Przecinek oddziela kolejne elementy, które chcemy wypisać.

```python
imie = "Jan"
wiek = 16

print("Mam na imię", imie, "i mam", wiek, "lat.")
```

Elementy w tym przykładzie:

Pierwszy element to tekst `"Mam na imię"`.

Drugi element to zmienna `imie`.

Trzeci element to tekst `"i mam"`.

Czwarty element to zmienna `wiek`.

Piąty element to tekst `"lat."`.

Przecinki mówią Pythonowi, że to są osobne elementy do wypisania.

Python sam dodaje spacje między elementami.

Wynik działania programu:

```text
Mam na imię Jan i mam 16 lat.
```

Drugi przykład:

```python
a = 5
b = 3
suma = a + b

print("Suma liczb", a, "i", b, "wynosi", suma)
```

Przecinki pozwalają wygodnie połączyć tekst, liczby i zmienne bez zamiany liczb na tekst.

Nie piszemy:

```python
print("Suma wynosi" suma)
```

W tym kodzie brakuje przecinka między tekstem a zmienną.

Poprawna wersja:

```python
print("Suma wynosi", suma)
```

## print() a nowy wiersz

Każde osobne wywołanie `print()` domyślnie wypisuje tekst w nowym wierszu.

```python
print("Pierwszy wiersz")
print("Drugi wiersz")
print("Trzeci wiersz")
```

Wynik:

```text
Pierwszy wiersz
Drugi wiersz
Trzeci wiersz
```

## Pusty print()

```python
print()
```

Pusty `print()` wypisuje pusty wiersz. Może służyć do oddzielenia fragmentów wyniku.

```python
print("Dane ucznia")
print()
print("Imię: Jan")
print("Wiek: 16")
```

## Wynik obliczenia w print()

```python
a = 5
b = 3
print("Wynik dodawania:", a + b)
```

Python najpierw obliczy `a + b`, a potem wypisze wynik obok tekstu.

## Formatowanie tekstu - dla chętnych

Gdy umiemy już podstawowe `print()` z przecinkami, możemy poznać wygodniejszy zapis: f-string.

Na początku wystarczy znać `print()` z przecinkami. F-stringi są dodatkiem dla osób, które chcą pisać czytelniej.

```python
imie = "Anna"
wiek = 16

print(f"Mam na imię {imie} i mam {wiek} lat.")
```

Omówienie:

Przed tekstem stawiamy literę `f`.

Wartości zmiennych wpisujemy w nawiasach klamrowych.

`{imie}` zostanie zastąpione wartością zmiennej `imie`.

`{wiek}` zostanie zastąpione wartością zmiennej `wiek`.

Przykład z obliczeniem:

```python
a = 5
b = 3
suma = a + b

print(f"Suma liczb {a} i {b} wynosi {suma}.")
```

Przykład zaokrąglania liczby:

```python
cena = 19.987

print(f"Cena wynosi {cena:.2f} zł")
```

Zapis `:.2f` oznacza pokazanie liczby z dwoma miejscami po kropce.

## Kiedy używać przecinków, a kiedy f-stringów?

Na początku używamy `print()` z przecinkami.

Przecinki są proste i bezpieczne.

F-stringi są wygodne, gdy chcemy ładnie sformatować całe zdanie.

F-stringi są szczególnie przydatne przy dłuższych komunikatach i zaokrąglaniu liczb.

Wersja podstawowa:

```python
print("Mam na imię", imie, "i mam", wiek, "lat.")
```

Wersja z f-stringiem:

```python
print(f"Mam na imię {imie} i mam {wiek} lat.")
```

Obie wersje są poprawne.

## Tekst czy zmienna?

```python
print("Mam", wiek, "lat.")
```

W tym przykładzie `wiek` jest zmienną. Python wypisze wartość zmiennej.

```python
print("Mam, wiek, lat.")
```

W tym przykładzie wszystko jest jednym tekstem. Python wypisze dokładnie napis: `Mam, wiek, lat.`

## Typowe błędy uczniów

### Brak cudzysłowu przy tekście

```python
print(Cześć)
```

Tekst musi być w cudzysłowie:

```python
print("Cześć")
```

### Brak przecinka między tekstem a zmienną

```python
imie = "Anna"
print("Cześć" imie)
```

Między tekstem a zmienną trzeba dodać przecinek:

```python
print("Cześć", imie)
```

### Mylenie tekstu ze zmienną

```python
imie = "Anna"
print("imie")
print(imie)
```

Pierwszy `print()` wypisze tekst `imie`.

Drugi `print()` wypisze wartość zmiennej, czyli `Anna`.

### Próba wypisania zmiennej, która nie istnieje

```python
print(wiek)
```

Jeśli wcześniej nie utworzono zmiennej `wiek`, program zgłosi błąd.

### Niepotrzebne wpisywanie liczby w cudzysłowie

```python
print("2026")
```

Ten zapis wypisze tekst. Jeśli chcemy używać liczby w obliczeniach, zapisujemy ją bez cudzysłowu.

### Myślenie, że przecinek w print() jest wypisywany

```python
print("Ala", "ma", "kota")
```

Przecinki oddzielają elementy w kodzie. Nie pojawią się na ekranie jako przecinki.

### Mylenie przecinka w print() z przecinkiem w tekście

```python
print("Cześć,", imie)
```

Przecinek w tekście `"Cześć,"` zostanie wypisany na ekranie. Przecinek po tekście oddziela elementy funkcji `print()`.

### Zapomnienie litery f przed f-stringiem

```python
imie = "Anna"
print("Mam na imię {imie}.")
```

Bez litery `f` Python wypisze nawiasy klamrowe jako zwykły tekst.

Poprawnie:

```python
print(f"Mam na imię {imie}.")
```

### Błędne nawiasy klamrowe w f-stringu

W f-stringu zmienne wpisujemy w nawiasach klamrowych, na przykład `{imie}`.

### Mylenie kropki i przecinka w liczbach rzeczywistych

W Pythonie liczby rzeczywiste zapisujemy z kropką, na przykład `19.99`.

## Ćwiczenia

1. Wypisz na ekranie tekst: Witaj w Pythonie!
2. Wypisz swoje imię.
3. Utwórz zmienną imie i wypisz ją za pomocą print().
4. Utwórz zmienne imie i wiek, a następnie wypisz zdanie: Mam na imię ... i mam ... lat.
5. Utwórz zmienne a i b, oblicz ich sumę i wypisz wynik w czytelnym komunikacie.
6. Utwórz zmienne dlugosc i szerokosc, oblicz pole prostokąta i wypisz wynik.
7. Wypisz trzy różne komunikaty, każdy w osobnym wierszu.
8. Użyj pustego print(), aby oddzielić nagłówek od danych.
9. Dla chętnych: wypisz zdanie z użyciem f-stringa.
10. Dla chętnych: wypisz cenę z dwoma miejscami po kropce za pomocą f-stringa.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
