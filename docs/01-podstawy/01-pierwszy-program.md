# Pierwszy program w Pythonie - komputer wykonuje Twoje polecenia

## Cel lekcji

Napiszesz i uruchomisz swój pierwszy program w Pythonie. Zobaczysz, że programowanie zaczyna się od wydawania komputerowi prostych i dokładnych poleceń.

## Czym jest program

Programowanie nie zaczyna się od trudnych algorytmów. Zaczyna się od bardzo prostej rzeczy: wydania komputerowi polecenia.

Komputer nie domyśla się, co masz na myśli. Wykonuje dokładnie to, co zapiszesz. Dlatego programista musi pisać jasno, dokładnie i w odpowiedniej kolejności.

Program to zestaw poleceń dla komputera.

Program można porównać do przepisu albo instrukcji obsługi. Jeśli w przepisie pomylisz kolejność kroków, efekt może być inny. Jeśli w programie pomylisz zapis, komputer nie zgadnie, co chciałeś zrobić.

## Pierwszy program

```python
print("Witaj w Pythonie!")
```

Omówienie:

`print` oznacza polecenie wypisania czegoś na ekranie.

Tekst umieszczamy w cudzysłowie.

Nawiasy są częścią zapisu funkcji `print()`.

Po uruchomieniu programu zobaczymy tekst: `Witaj w Pythonie!`

## Instrukcja programu

Instrukcja to pojedyncze polecenie w programie.

W tym przykładzie instrukcją jest cały zapis:

```python
print("Witaj w Pythonie!")
```

Program może mieć jedną instrukcję albo wiele instrukcji.

```python
print("Start programu")
print("Uczę się Pythona")
print("Koniec programu")
```

Python wykonuje instrukcje od góry do dołu.

Najpierw wypisze pierwszy tekst.

Potem drugi.

Potem trzeci.

Kolejność w programie ma znaczenie.

## Zmiana tekstu w programie

Możesz zmienić tekst zapisany w cudzysłowie.

```python
print("To jest mój pierwszy program.")
```

Jeśli zmienisz tekst w cudzysłowie, program wypisze nową wiadomość.

W kolejnych lekcjach nauczysz się też zapamiętywać dane w zmiennych i wykonywać obliczenia.

## Komputer nie zgaduje

Komputer nie wie, co autor programu miał na myśli.

Jeżeli zapiszemy polecenie błędnie, Python zgłosi błąd. To normalna część nauki programowania.

Błąd nie oznacza porażki. Błąd oznacza, że trzeba poprawić zapis.

## Pierwsze typowe błędy

### Brak nawiasu

```python
print("Cześć!"
```

Brakuje zamykającego nawiasu.

Python nie może poprawnie odczytać instrukcji.

Trzeba dopisać brakujący nawias.

Poprawna wersja:

```python
print("Cześć!")
```

### Literówka w print

```python
pritn("Cześć!")
```

W nazwie `print` jest literówka.

Python nie rozpoznaje polecenia `pritn`.

Poprawna nazwa to `print`.

Poprawna wersja:

```python
print("Cześć!")
```

### Brak cudzysłowu przy tekście

```python
print(Cześć!)
```

Tekst powinien być zapisany w cudzysłowie.

Bez cudzysłowu Python próbuje traktować `Cześć` jako nazwę.

Poprawnie zapisujemy tekst tak:

```python
print("Cześć!")
```

## Jak czytać pierwszy program?

Przykład:

```python
print("Python działa!")
```

Można go przeczytać tak:

Wypisz na ekranie tekst `Python działa!`

Nie trzeba jeszcze rozumieć całego Pythona.

Na początku ważne jest, aby umieć uruchomić prostą instrukcję.

Potem będziemy stopniowo dodawać zmienne, obliczenia, warunki i pętle.

## Pierwsze eksperymenty

Zmieniaj tekst w cudzysłowie i obserwuj wynik.

```python
print("To jest mój pierwszy program.")
print("Python wykonuje moje polecenia.")
print("Programowanie zaczyna się od jednej instrukcji.")
```

Możesz zmieniać tekst, ale zostaw:

nazwę `print`,

nawiasy,

cudzysłowy wokół tekstu.

## JupyterLab i plik .py

W JupyterLab możemy uruchamiać kod w komórkach. To wygodne podczas nauki, bo szybko widzimy wynik.

Ten sam kod można też zapisać w pliku z rozszerzeniem `.py`, na przykład:

```text
pierwszy_program.py
```

Taki plik można uruchomić jako zwykły program w Pythonie.

Na zajęciach będziemy korzystać głównie z JupyterLab, a później także z plików `.py`.

## Typowe błędy uczniów

### Literówka w nazwie print

Python zna polecenie `print`, ale nie zna `pritn`.

### Brak nawiasu otwierającego lub zamykającego

Nawiasy muszą być kompletne.

### Brak cudzysłowu przy tekście

Tekst zapisujemy w cudzysłowie.

### Różne cudzysłowy na początku i końcu tekstu

Na początku i na końcu tekstu użyj takiego samego cudzysłowu.

### Dopisanie tekstu poza nawiasem

Cały tekst, który ma wypisać `print()`, powinien być zapisany wewnątrz nawiasów.

### Myślenie, że Python sam poprawi błąd

Python nie zgaduje. Trzeba poprawić zapis samodzielnie.

### Strach przed komunikatem błędu

Komunikat błędu to wskazówka. Pomaga znaleźć miejsce, które trzeba poprawić.

### Przypadkowe usunięcie jednego znaku

W programowaniu jeden znak może mieć znaczenie.

### Dziwne znaki w kodzie

W kodzie używamy zwykłych znaków, takich jak proste cudzysłowy i nawiasy.

### Brak uruchomienia komórki w JupyterLab

Jeśli nie uruchomisz komórki, program się nie wykona.

## Najważniejsza myśl z tej lekcji

Program to zestaw dokładnych poleceń dla komputera. Python wykonuje je w takiej kolejności, w jakiej zostały zapisane. Pierwszym poleceniem, którego używamy, jest `print()`, czyli wypisanie informacji na ekranie.

## Ćwiczenia

1. Uruchom program wypisujący tekst: Witaj w Pythonie!
2. Zmień tekst na swoje imię.
3. Wypisz trzy zdania, każde w osobnej instrukcji print().
4. Napisz program, który wypisuje nazwę szkoły, klasę i swoje imię.
5. Napisz program, który wypisuje krótki komunikat: To jest mój pierwszy program w Pythonie.
6. Celowo usuń jeden nawias z programu, uruchom go i zobacz komunikat błędu. Potem popraw program.
7. Celowo wpisz pritn zamiast print, uruchom program i zobacz komunikat błędu. Potem popraw program.
8. Napisz program, który wypisuje krótki plan dnia w trzech liniach.
9. Napisz program, który wypisuje tytuł ulubionej gry, filmu albo książki.
10. Napisz program, który wypisuje zdanie: Komputer wykonuje dokładnie to, co zapiszę.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
