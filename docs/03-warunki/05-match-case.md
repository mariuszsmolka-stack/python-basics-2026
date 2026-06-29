# match-case w Pythonie — wybór jednej z wielu możliwości

## Cel lekcji

Celem lekcji jest poznanie konstrukcji `match-case`, która pozwala wybrać jedną z kilku możliwych wartości w czytelny sposób.

## Czego się nauczysz

Po tej lekcji będziesz umieć:

1. wyjaśnić, czym jest `match-case`,
2. zapisać prostą konstrukcję `match-case`,
3. używać `case _` jako przypadku domyślnego,
4. porównać `match-case` z `if-elif-else`,
5. wybrać, kiedy lepiej użyć `match-case`, a kiedy zostać przy `if-elif-else`.

## Krótkie przypomnienie if-elif-else

Instrukcja `if-elif-else` pozwala sprawdzać kilka warunków po kolei.

Przykład:

```python
wybor = int(input("Wybierz opcję: "))

if wybor == 1:
    print("Start")
elif wybor == 2:
    print("Ustawienia")
elif wybor == 3:
    print("Koniec")
else:
    print("Nieznana opcja")
```

Ten zapis jest poprawny i często wystarcza. W prostych programach można używać `if-elif-else` bez problemu.

Czasami jednak sprawdzamy jedną zmienną i wiele konkretnych wartości. Wtedy `match-case` może być czytelniejsze.

## Czym jest match-case?

W Pythonie nie piszemy `switch` tak jak w niektórych innych językach.

W Pythonie od wersji 3.10 istnieje konstrukcja `match-case`. Może ona pełnić podobną rolę.

`match-case` sprawdza wartość i dopasowuje ją do jednego z przypadków.

Najprościej:

1. `match` mówi, jaką wartość sprawdzamy,
2. `case` mówi, co zrobić dla konkretnej wartości,
3. `case _` oznacza przypadek domyślny, czyli każdą inną wartość.

## Podstawowa składnia

Przykład:

```python
wybor = int(input("Wybierz opcję: "))

match wybor:
    case 1:
        print("Start programu")
    case 2:
        print("Ustawienia")
    case 3:
        print("Koniec")
    case _:
        print("Nieznana opcja")
```

Omówienie:

1. `match wybor` oznacza: sprawdź wartość zmiennej `wybor`.
2. `case 1` wykona się, gdy `wybor` ma wartość 1.
3. `case 2` wykona się, gdy `wybor` ma wartość 2.
4. `case 3` wykona się, gdy `wybor` ma wartość 3.
5. `case _` oznacza przypadek domyślny, czyli każdą inną wartość.
6. Po `match` i po każdym `case` stawiamy dwukropek.
7. Instrukcje pod `case` muszą być wcięte.

## Jak czytać match-case?

Przykład:

```python
match wybor:
    case 1:
        print("Start")
    case 2:
        print("Ustawienia")
    case _:
        print("Nieznana opcja")
```

Można to przeczytać tak:

Sprawdź wartość zmiennej `wybor`. Jeżeli wynosi 1, wypisz `Start`. Jeżeli wynosi 2, wypisz `Ustawienia`. W każdym innym przypadku wypisz `Nieznana opcja`.

## Przykład prostego menu

```python
wybor = int(input("Wybierz opcję: "))

match wybor:
    case 1:
        print("Start programu")
    case 2:
        print("Pomoc")
    case 3:
        print("Koniec programu")
    case _:
        print("Nieznana opcja")
```

Omówienie:

1. Użytkownik wpisuje numer opcji.
2. Program sprawdza wartość zmiennej `wybor`.
3. Dla wartości 1, 2 albo 3 wykonuje odpowiedni komunikat.
4. Dla każdej innej wartości wykonuje się `case _`.

## Przykład dni tygodnia

```python
dzien = int(input("Podaj numer dnia tygodnia od 1 do 7: "))

match dzien:
    case 1:
        print("Poniedziałek")
    case 2:
        print("Wtorek")
    case 3:
        print("Środa")
    case 4:
        print("Czwartek")
    case 5:
        print("Piątek")
    case 6:
        print("Sobota")
    case 7:
        print("Niedziela")
    case _:
        print("Nieprawidłowy numer dnia")
```

Omówienie:

1. Program wczytuje numer dnia tygodnia.
2. `match dzien` sprawdza wpisaną wartość.
3. Każdy `case` odpowiada jednemu numerowi dnia.
4. `case _` obsługuje błędny numer, na przykład 0 albo 9.

## Przykład wyboru działania w kalkulatorze

```python
a = float(input("Podaj pierwszą liczbę: "))
b = float(input("Podaj drugą liczbę: "))

print("1 — dodawanie")
print("2 — odejmowanie")
print("3 — mnożenie")
print("4 — dzielenie")

wybor = int(input("Wybierz działanie: "))

match wybor:
    case 1:
        print("Wynik:", a + b)
    case 2:
        print("Wynik:", a - b)
    case 3:
        print("Wynik:", a * b)
    case 4:
        print("Wynik:", a / b)
    case _:
        print("Nieznane działanie")
```

Ten przykład nie sprawdza jeszcze dzielenia przez zero. Taki przypadek można omówić osobno.

## case _ jako odpowiednik "w innym przypadku"

Zapis `case _` działa podobnie jak `else` w instrukcji `if-elif-else`.

Oznacza: jeśli żaden wcześniejszy przypadek nie pasuje, wykonaj ten fragment.

Przykład:

```python
wybor = int(input("Wybierz opcję: "))

match wybor:
    case 1:
        print("Wybrano opcję 1")
    case _:
        print("Nieznana opcja")
```

Warto dodawać `case _`, gdy użytkownik może wpisać wartość spoza menu.

## if-elif-else czy match-case?

Wersja z `if-elif-else`:

```python
wybor = int(input("Wybierz opcję: "))

if wybor == 1:
    print("Start")
elif wybor == 2:
    print("Ustawienia")
elif wybor == 3:
    print("Koniec")
else:
    print("Nieznana opcja")
```

Wersja z `match-case`:

```python
wybor = int(input("Wybierz opcję: "))

match wybor:
    case 1:
        print("Start")
    case 2:
        print("Ustawienia")
    case 3:
        print("Koniec")
    case _:
        print("Nieznana opcja")
```

Oba programy robią podobną rzecz.

`if-elif-else` jest bardziej uniwersalne.

`match-case` bywa czytelne, gdy sprawdzamy jedną zmienną i kilka konkretnych wartości.

## Kiedy używać match-case?

`match-case` warto używać:

1. gdy sprawdzamy jedną zmienną,
2. gdy mamy kilka konkretnych wartości,
3. gdy tworzymy proste menu,
4. gdy chcemy poprawić czytelność długiego `if-elif-else`.

## Kiedy zostać przy if-elif-else?

Przy `if-elif-else` warto zostać:

1. gdy warunki są bardziej złożone,
2. gdy porównujemy zakresy, na przykład `punkty >= 90`,
3. gdy sprawdzamy kilka różnych zmiennych,
4. gdy uczymy się podstaw i chcemy najpierw dobrze opanować `if`, `elif` i `else`.

Przykład, gdzie lepsze jest `if-elif-else`:

```python
punkty = int(input("Podaj liczbę punktów: "))

if punkty >= 90:
    print("Bardzo dobry")
elif punkty >= 75:
    print("Dobry")
elif punkty >= 50:
    print("Dostateczny")
else:
    print("Brak zaliczenia")
```

Tutaj sprawdzamy zakresy punktów. Dlatego `if-elif-else` jest naturalniejsze.

## Typowe błędy uczniów

1. Pisanie `switch` zamiast `match`.
2. Brak dwukropka po `match`.
3. Brak dwukropka po `case`.
4. Brak wcięć.
5. Zapomnienie o `case _` dla nieznanej wartości.
6. Mylenie `case _` z `else`.
7. Używanie `match-case` tam, gdzie lepsze jest `if-elif-else`.
8. Próba sprawdzania zakresów przez `match-case`, gdy prościej użyć `if`.
9. Brak konwersji `int()` przy wyborze opcji.
10. Myślenie, że `match-case` jest obowiązkowe.

## Najważniejsza zasada

`match-case` jest wygodne, gdy wybieramy jedną z kilku konkretnych wartości. Nie zastępuje całkowicie `if-elif-else`.

## Ćwiczenia dla ucznia

### A. Zadania proste

1. Napisz menu z opcjami: 1 — start, 2 — pomoc, 3 — koniec.
2. Wczytaj numer dnia tygodnia i wypisz jego nazwę.
3. Wczytaj numer miesiąca od 1 do 12 i wypisz nazwę miesiąca.
4. Wczytaj ocenę od 1 do 6 i wypisz jej opis słowny.
5. Wczytaj numer kierunku: 1 — północ, 2 — południe, 3 — wschód, 4 — zachód.

### B. Zadania średnie

1. Napisz prosty kalkulator z wyborem działania przez numer.
2. Napisz menu programu szkolnego: 1 — oceny, 2 — frekwencja, 3 — plan lekcji, 4 — wyjście.
3. Wczytaj numer poziomu trudności gry i wypisz opis poziomu.
4. Wczytaj kod produktu i wypisz nazwę produktu.
5. Wczytaj numer figury: 1 — kwadrat, 2 — prostokąt, 3 — koło, i wypisz, jakie dane trzeba podać do obliczenia pola.

### C. Zadania trochę trudniejsze

1. Rozbuduj kalkulator o obsługę błędnej opcji.
2. Napisz program wyboru biletu: 1 — normalny, 2 — ulgowy, 3 — rodzinny.
3. Napisz menu mini-gry tekstowej z kilkoma wyborami.
4. Porównaj własny program z `if-elif-else` i z `match-case`.
5. Napisz program, w którym `match-case` obsługuje komendy tekstowe: `start`, `pomoc`, `koniec`.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania w swoim folderze w JupyterLab.

Każde zadanie powinno być zapisane w osobnym pliku `.py` albo wyraźnie oddzielone w notebooku.

Proponowane nazwy plików:

```text
match_case_a01.py
match_case_b01.py
match_case_c01.py
```
