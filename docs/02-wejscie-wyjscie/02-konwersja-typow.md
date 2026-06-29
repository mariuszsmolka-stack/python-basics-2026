# Konwersja typów w Pythonie - int(), float(), str()

## Cel lekcji

Poznasz konwersję typów i nauczysz się zamieniać dane na taki typ, który jest potrzebny w programie.

## Czego się nauczysz

Po tej lekcji będziesz umieć zamieniać tekst na liczbę całkowitą za pomocą `int()`, tekst na liczbę rzeczywistą za pomocą `float()` oraz liczbę na tekst za pomocą `str()`. Zobaczysz też, dlaczego jest to ważne przy danych wczytywanych funkcją `input()`.

## Przypomnienie o input()

Funkcja `input()` zawsze zwraca tekst, czyli typ `str`. Oznacza to, że nawet jeśli użytkownik wpisze `2`, Python najpierw zapamięta tę wartość jako tekst `"2"`, a nie jako liczbę.

Gdy chcemy wykonywać obliczenia, często musimy zamienić tekst na liczbę.

## Czym jest konwersja typów

Konwersja typów to zamiana wartości z jednego typu na inny typ.

W Pythonie często używamy trzech prostych konwersji:

`int()` stosujemy do liczb całkowitych.

`float()` stosujemy do liczb rzeczywistych.

`str()` stosujemy, gdy chcemy zamienić wartość na tekst.

## Po co zamieniamy tekst na liczby

Dane wpisane przez użytkownika są tekstem. Jeśli chcemy je dodać, odjąć, pomnożyć albo podzielić, musimy najpierw zamienić je na liczby.

Bez konwersji Python może potraktować wpisane dane jak zwykłe napisy.

## Funkcja int()

Funkcja `int()` zamienia tekst na liczbę całkowitą.

```python
liczba = int(input("Podaj liczbę całkowitą: "))
print("Podana liczba to:", liczba)
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wyświetla komunikat, pobiera dane od użytkownika i zamienia wpisany tekst na liczbę całkowitą.

Drugi wiersz wypisuje wartość zmiennej `liczba`.

## Funkcja float()

Funkcja `float()` zamienia tekst na liczbę rzeczywistą, czyli liczbę z częścią dziesiętną.

```python
wzrost = float(input("Podaj wzrost w metrach: "))
print("Twój wzrost to:", wzrost)
```

W Pythonie część dziesiętną zapisujemy z kropką, na przykład `1.75`, a nie z przecinkiem.

## Funkcja str()

Funkcja `str()` zamienia wartość na tekst.

Jest przydatna wtedy, gdy chcemy połączyć tekst z liczbą za pomocą znaku `+`.

```python
wiek = 16
tekst = "Mam " + str(wiek) + " lat."
print(tekst)
```

Bez `str(wiek)` Python zgłosi błąd, bo nie można bezpośrednio połączyć tekstu z liczbą za pomocą znaku `+`.

Omówienie wiersz po wierszu:

Pierwszy wiersz zapisuje liczbę w zmiennej `wiek`.

Drugi wiersz zamienia liczbę na tekst i łączy ją z innymi tekstami.

Trzeci wiersz wyświetla gotowe zdanie.

## Błąd: dodawanie bez konwersji

```python
a = input("Podaj pierwszą liczbę: ")
b = input("Podaj drugą liczbę: ")
print(a + b)
```

Jeżeli użytkownik wpisze `2` i `3`, program wypisze `23`, ponieważ Python potraktuje dane jako teksty. Znak `+` połączy wtedy dwa teksty, zamiast dodać dwie liczby.

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje pierwszą wartość jako tekst.

Drugi wiersz wczytuje drugą wartość jako tekst.

Trzeci wiersz łączy dwa teksty.

## Poprawne dodawanie liczb całkowitych

```python
a = int(input("Podaj pierwszą liczbę: "))
b = int(input("Podaj drugą liczbę: "))
print(a + b)
```

Funkcja `int()` zamienia tekst na liczbę całkowitą. Dzięki temu Python wykonuje dodawanie matematyczne.

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje pierwszą liczbę i zamienia ją na typ `int`.

Drugi wiersz wczytuje drugą liczbę i zamienia ją na typ `int`.

Trzeci wiersz wypisuje sumę liczb.

## Średnia dwóch ocen

```python
ocena1 = float(input("Podaj pierwszą ocenę: "))
ocena2 = float(input("Podaj drugą ocenę: "))
srednia = (ocena1 + ocena2) / 2
print("Średnia ocen wynosi:", srednia)
```

W tym przykładzie używamy `float()`, ponieważ ocena może mieć część dziesiętną, na przykład `4.5`.

## Pole prostokąta

```python
a = float(input("Podaj długość pierwszego boku: "))
b = float(input("Podaj długość drugiego boku: "))
pole = a * b
print("Pole prostokąta wynosi:", pole)
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje długość pierwszego boku jako liczbę rzeczywistą.

Drugi wiersz wczytuje długość drugiego boku jako liczbę rzeczywistą.

Trzeci wiersz oblicza pole prostokąta.

Czwarty wiersz wyświetla wynik.

## Cena brutto z ceny netto

```python
cena_netto = float(input("Podaj cenę netto: "))
cena_brutto = cena_netto * 1.23
print("Cena brutto wynosi:", cena_brutto)
```

Program wczytuje cenę netto jako liczbę rzeczywistą. Następnie mnoży ją przez `1.23`, czyli dolicza podatek 23%.

## Przeliczanie minut na godziny i minuty

```python
minuty = int(input("Podaj liczbę minut: "))
godziny = minuty // 60
pozostale_minuty = minuty % 60
print("To jest", godziny, "godzin i", pozostale_minuty, "minut.")
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje liczbę minut jako liczbę całkowitą.

Drugi wiersz oblicza pełne godziny za pomocą dzielenia całkowitego `//`.

Trzeci wiersz oblicza pozostałe minuty za pomocą reszty z dzielenia `%`.

Czwarty wiersz wyświetla wynik.

## Wiek na podstawie roku urodzenia

```python
rok_urodzenia = int(input("Podaj rok urodzenia: "))
wiek = 2026 - rok_urodzenia
print("Twój przybliżony wiek to:", wiek)
```

Program wczytuje rok urodzenia jako liczbę całkowitą. Potem odejmuje go od roku `2026` i wyświetla przybliżony wiek użytkownika.

## Typowe błędy uczniów

### Brak konwersji po input()

Po `input()` dane są tekstem. Do obliczeń trzeba użyć `int()` albo `float()`.

```python
a = input("Podaj liczbę: ")
print(a + a)
```

Ten kod łączy tekst z tekstem. Nie wykonuje dodawania liczb.

### Użycie int() do liczby z częścią dziesiętną

```python
liczba = int("3.5")
```

Taki zapis spowoduje błąd. Do liczby `3.5` trzeba użyć `float()`, a nie `int()`.

### Wpisanie przecinka zamiast kropki

```python
liczba = float(input("Podaj liczbę rzeczywistą: "))
```

W Pythonie należy wpisać `3.5`, a nie `3,5`. Przecinek nie jest poprawnym znakiem części dziesiętnej.

### Próba łączenia tekstu z liczbą bez str()

```python
wiek = 16
tekst = "Mam " + wiek + " lat."
print(tekst)
```

Ten kod spowoduje błąd. Poprawny zapis wymaga `str(wiek)`.

```python
wiek = 16
tekst = "Mam " + str(wiek) + " lat."
print(tekst)
```

### Mylenie / oraz //

Operator `/` wykonuje zwykłe dzielenie.

Operator `//` wykonuje dzielenie całkowite.

```python
print(7 / 2)
print(7 // 2)
```

Pierwszy wynik to `3.5`. Drugi wynik to `3`, ponieważ `//` zwraca tylko pełną część dzielenia.

## Ćwiczenia

1. Wczytaj dwie liczby całkowite i wypisz ich sumę.
2. Wczytaj dwie liczby całkowite i wypisz ich różnicę, iloczyn oraz iloraz.
3. Wczytaj dwie oceny i oblicz ich średnią.
4. Wczytaj długość boku kwadratu i oblicz jego pole.
5. Wczytaj długości boków prostokąta i oblicz jego pole.
6. Wczytaj cenę netto i oblicz cenę brutto przy podatku 23%.
7. Wczytaj liczbę minut i przelicz ją na godziny oraz minuty.
8. Wczytaj rok urodzenia i oblicz przybliżony wiek.
9. Wczytaj liczbę kilometrów i przelicz ją na metry.
10. Wczytaj imię oraz wiek, a następnie wypisz zdanie typu: Mam na imię Jan i mam 16 lat.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
