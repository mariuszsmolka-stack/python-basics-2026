# Wczytywanie danych od użytkownika - input()

## Cel lekcji

Poznasz funkcję `input()` i nauczysz się wczytywać dane wpisane przez użytkownika z klawiatury.

## Czego się nauczysz

Po tej lekcji będziesz umieć używać funkcji `input()` z komunikatem dla użytkownika. Dowiesz się, że `input()` zawsze zwraca tekst, czyli typ `str`. Nauczysz się też zamieniać wpisany tekst na liczbę całkowitą za pomocą `int()` oraz na liczbę rzeczywistą za pomocą `float()`.

## Do czego służy input()

Funkcja `input()` służy do wczytywania danych od użytkownika. Program zatrzymuje się i czeka, aż użytkownik wpisze coś z klawiatury oraz zatwierdzi wpis klawiszem Enter.

Ważne jest to, że `input()` zawsze zwraca tekst, czyli wartość typu `str`. Nawet jeśli użytkownik wpisze liczbę, Python najpierw potraktuje ją jak tekst.

## Komunikat w funkcji input()

Tekst zapisany w nawiasie funkcji `input()` to komunikat dla użytkownika. Taki komunikat nazywa się też promptem. Dzięki niemu użytkownik wie, co ma wpisać.

Przykład bez komunikatu:

```python
imie = input()
print("Cześć,", imie)
```

Ten zapis działa, ale jest mało czytelny. Użytkownik widzi tylko puste miejsce do wpisania danych i może nie wiedzieć, co powinien podać.

Przykład z komunikatem:

```python
imie = input("Podaj swoje imię: ")
print("Cześć,", imie)
```

W tym przykładzie program wyświetla komunikat `Podaj swoje imię: `. Użytkownik wpisuje imię, a program zapisuje je w zmiennej `imie`.

Omówienie wiersz po wierszu:

Pierwszy wiersz wyświetla komunikat i czeka na wpisanie imienia.

Wpisane imię trafia do zmiennej `imie`.

Drugi wiersz wypisuje powitanie oraz wartość zmiennej `imie`.

## Wczytanie imienia i wypisanie powitania

```python
imie = input("Jak masz na imię? ")
print("Witaj,", imie)
```

Program pyta użytkownika o imię, a potem wypisuje krótkie powitanie. Zmienna `imie` przechowuje tekst wpisany przez użytkownika.

## Wczytanie wieku jako tekstu

```python
wiek = input("Podaj swój wiek: ")
print("Masz", wiek, "lat")
```

W tym przykładzie zmienna `wiek` przechowuje tekst. Jeśli użytkownik wpisze `15`, to dla Pythona nadal będzie to tekst `"15"`, a nie liczba.

## Wczytanie liczby całkowitej

```python
liczba = int(input("Podaj liczbę całkowitą: "))
print("Podana liczba to:", liczba)
```

Ten zapis jest bardzo ważny:

```python
liczba = int(input("Podaj liczbę całkowitą: "))
```

Oznacza on, że najpierw wyświetlany jest komunikat `Podaj liczbę całkowitą: `. Potem użytkownik wpisuje dane z klawiatury. Funkcja `input()` zwraca wpisane dane jako tekst. Funkcja `int()` zamienia ten tekst na liczbę całkowitą. Wynik trafia do zmiennej `liczba`.

Omówienie wiersz po wierszu:

Pierwszy wiersz pobiera dane od użytkownika i zamienia je na liczbę całkowitą.

Drugi wiersz wyświetla wartość zapisaną w zmiennej `liczba`.

## Wczytanie liczby rzeczywistej

Do wczytywania liczb z częścią dziesiętną używamy funkcji `float()`.

```python
wzrost = float(input("Podaj wzrost w metrach: "))
print("Twój wzrost to:", wzrost)
```

Jeśli użytkownik wpisze `1.75`, funkcja `input()` najpierw zwróci tekst `"1.75"`. Funkcja `float()` zamieni ten tekst na liczbę rzeczywistą.

## Pole prostokąta

```python
a = float(input("Podaj długość pierwszego boku: "))
b = float(input("Podaj długość drugiego boku: "))
pole = a * b
print("Pole prostokąta wynosi:", pole)
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje długość pierwszego boku i zamienia ją na liczbę rzeczywistą.

Drugi wiersz wczytuje długość drugiego boku i zamienia ją na liczbę rzeczywistą.

Trzeci wiersz oblicza pole prostokąta przez pomnożenie boków.

Czwarty wiersz wyświetla wynik obliczeń.

## Wiek na podstawie roku urodzenia

```python
rok_urodzenia = int(input("Podaj rok urodzenia: "))
rok_obecny = 2026
wiek = rok_obecny - rok_urodzenia
print("Twój przybliżony wiek to:", wiek)
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje rok urodzenia i zamienia go na liczbę całkowitą.

Drugi wiersz zapisuje obecny rok w zmiennej `rok_obecny`.

Trzeci wiersz oblicza przybliżony wiek użytkownika.

Czwarty wiersz wyświetla wynik.

## Typowe problemy uczniów

### Użycie input() bez komunikatu

```python
wiek = input()
```

Taki zapis działa, ale użytkownik nie wie, co ma wpisać. Lepiej dodać komunikat:

```python
wiek = input("Podaj swój wiek: ")
```

### Próba dodawania liczb bez konwersji

```python
a = input("Podaj pierwszą liczbę: ")
b = input("Podaj drugą liczbę: ")
print(a + b)
```

W tym przykładzie Python łączy teksty zamiast dodawać liczby. Jeśli użytkownik wpisze `2` i `3`, wynik może wyglądać jak `23`, a nie `5`.

Poprawny zapis:

```python
a = int(input("Podaj pierwszą liczbę: "))
b = int(input("Podaj drugą liczbę: "))
print(a + b)
```

Tutaj `int()` zamienia wpisane teksty na liczby całkowite. Dopiero wtedy Python wykonuje dodawanie matematyczne.

### Wpisanie złego rodzaju danych

```python
liczba = int(input("Podaj liczbę całkowitą: "))
```

Jeśli użytkownik wpisze tekst zamiast liczby, program nie będzie mógł zamienić go na liczbę całkowitą. Dlatego trzeba czytać komunikaty i wpisywać dane zgodnie z poleceniem.

## Ćwiczenia

1. Wczytaj imię i wypisz powitanie.
2. Wczytaj imię i nazwisko, a następnie wypisz je w jednym zdaniu.
3. Wczytaj dwie liczby całkowite i wypisz ich sumę.
4. Wczytaj dwie liczby rzeczywiste i oblicz ich średnią.
5. Wczytaj długość boku kwadratu i oblicz jego pole.
6. Wczytaj długości boków prostokąta i oblicz jego pole.
7. Wczytaj rok urodzenia i oblicz przybliżony wiek użytkownika.
8. Wczytaj cenę netto i oblicz cenę brutto przy podatku 23%.

## Sposób oddania pracy

Wykonaj ćwiczenia w JupyterLab. Gotowe rozwiązania zapisz w swoim folderze w JupyterLab.
