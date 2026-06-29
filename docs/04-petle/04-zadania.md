# Zadania - pętle while, for, range(), licznik i akumulator

## Cel lekcji

Utrwalisz używanie pętli `while`, pętli `for`, funkcji `range()`, licznika i akumulatora.

To jest lekcja ćwiczeniowa. Nie poznajesz tu nowej teorii, tylko rozwiązujesz zadania z pętlami.

## Czego używasz w tej lekcji

W zadaniach możesz używać:

- `print()`,
- zmiennych,
- `input()`,
- `int()`,
- `float()`,
- operatorów arytmetycznych,
- operatorów porównania,
- `if` / `else` / `elif`, jeśli zadanie tego wymaga,
- `while`,
- `for`,
- `range()`,
- licznika,
- akumulatora,
- skróconych operatorów przypisania, na przykład `+=`, `-=`, `*=`.

Nie używaj list, funkcji własnych, klas, plików, bibliotek zewnętrznych, `break` ani `continue`.

W zadaniach prostych i średnich nie używaj zagnieżdżonych pętli.

## Krótkie przypomnienie

- `while` działa dopóki warunek jest prawdziwy.
- `for` z `range()` wykonuje instrukcje dla kolejnych wartości.
- `range(5)` daje wartości `0`, `1`, `2`, `3`, `4`.
- `range(1, 6)` daje wartości `1`, `2`, `3`, `4`, `5`.
- `range(2, 11, 2)` daje wartości `2`, `4`, `6`, `8`, `10`.
- Licznik zwykle odpowiada na pytanie: ile razy?
- Akumulator przechowuje stopniowo budowany wynik, na przykład sumę.
- Zapis `suma += i` oznacza to samo co `suma = suma + i`.
- W pętli `while` trzeba pamiętać o zmianie zmiennej użytej w warunku.

## Zasady wykonywania zadań

1. Każde zadanie zapisz w osobnym pliku albo wyraźnie oddziel w notebooku.
2. Program ma wypisywać czytelne wyniki.
3. Używaj czytelnych nazw zmiennych.
4. Jeżeli zadanie wymaga pętli `for`, użyj `for` i `range()`.
5. Jeżeli zadanie wymaga pętli `while`, użyj `while`.
6. W zadaniach z sumą używaj akumulatora, na przykład `suma = 0`.
7. W zadaniach z iloczynem używaj akumulatora zaczynającego od `1`, na przykład `iloczyn = 1`.
8. Testuj program dla kilku danych.
9. Nie używaj list.
10. Nie używaj `break` ani `continue`.

Zadania są podzielone na poziomy. Nie każdy uczeń musi wykonać wszystkie zadania. Zadania proste sprawdzają podstawowe użycie pętli. Zadania średnie wymagają użycia licznika albo akumulatora. Zadania trochę trudniejsze są dla osób, które chcą powalczyć o wyższą ocenę.

# A. Zadania proste

Zadania proste sprawdzają, czy umiesz uruchomić pętlę i kontrolować jej przebieg.

## 1. Liczby od 1 do 10

Wypisz liczby od `1` do `10` za pomocą pętli `for`.

## 2. Liczby od 0 do 9

Wypisz liczby od `0` do `9` za pomocą pętli `for`.

## 3. Liczby od 1 do n

Wczytaj liczbę `n` i wypisz liczby od `1` do `n`.

## 4. Liczby od 10 do 1

Wypisz liczby od `10` do `1` za pomocą pętli `while`.

## 5. Liczby parzyste

Wypisz liczby parzyste od `2` do `20`.

## 6. Co drugi numer

Wypisz liczby `5`, `10`, `15`, `20`, `25`, `30`.

## 7. Powtórzenie komunikatu

Wczytaj imię użytkownika i wypisz 5 razy komunikat:

```text
Cześć, ...
```

## 8. Odliczanie

Wczytaj liczbę startową i odliczaj od niej do zera.

## 9. Tabliczka mnożenia jednej liczby

Wczytaj liczbę i wypisz jej tabliczkę mnożenia od `1` do `10`.

## 10. Kwadraty liczb

Wczytaj `n` i wypisz kwadraty liczb od `1` do `n`.

# B. Zadania średnie

Zadania średnie wymagają użycia licznika, akumulatora albo pętli z obliczeniami.

## 1. Suma od 1 do n

Wczytaj `n` i oblicz sumę liczb od `1` do `n`.

## 2. Iloczyn od 1 do n

Wczytaj `n` i oblicz iloczyn liczb od `1` do `n`.

## 3. Suma liczb parzystych

Wczytaj `n` i oblicz sumę liczb parzystych od `2` do `n`.

## 4. Suma kwadratów

Wczytaj `n` i oblicz sumę kwadratów liczb od `1` do `n`.

## 5. Licznik prób

Napisz program, który pyta użytkownika o hasło tak długo, aż wpisze `"python"`. Policz liczbę prób.

Nie używaj `break`.

## 6. Koszyk ze smartfonami

Wczytaj liczbę smartfonów w koszyku. Program ma wypisywać komunikat o rozdawaniu smartfonów, aż koszyk będzie pusty.

Przykład komunikatu:

```text
Rozdaję smartfon. Zostało: ...
```

## 7. Oszczędzanie

Wczytaj kwotę początkową, miesięczną wpłatę i liczbę miesięcy. Oblicz, ile pieniędzy będzie po podanej liczbie miesięcy.

## 8. Koszt kilku produktów

Wczytaj cenę produktu i liczbę sztuk. Oblicz koszt całkowity przez dodawanie ceny w pętli.

To zadanie celowo ćwiczy akumulator, nawet jeśli można je rozwiązać mnożeniem.

## 9. Średnia z kilku ocen

Wczytaj liczbę ocen `n`. Następnie w pętli wczytaj `n` ocen i oblicz średnią.

Nie używaj list. Użyj akumulatora `suma`.

## 10. Liczba kroków

Wczytaj cel kroków na dzień oraz liczbę dni. Dla każdego dnia wczytaj liczbę wykonanych kroków. Oblicz łączną liczbę kroków.

Nie używaj list.

# C. Zadania trochę trudniejsze

Te zadania wymagają dokładniejszego pilnowania warunku pętli, akumulatora, licznika i przypadków granicznych.

## 1. Zgadywanie liczby bez random

Ustal w programie tajną liczbę. Użytkownik zgaduje, aż trafi.

Program podpowiada:

- za mało,
- za dużo,
- poprawnie.

Program liczy liczbę prób.

Nie używaj `break`.

## 2. Zgadywanie liczby z limitem prób

Ustal tajną liczbę. Użytkownik ma maksymalnie `5` prób. Program kończy się, gdy użytkownik zgadnie albo wykorzysta wszystkie próby.

Nie używaj `break`. Użyj warunku w `while`.

## 3. Spłacanie długu

Wczytaj kwotę długu i miesięczną spłatę. Oblicz, po ilu miesiącach dług zostanie spłacony.

Uwaga: jeżeli rata nie dzieli długu równo, ostatni miesiąc też się liczy.

## 4. Dojście do celu oszczędności

Wczytaj cel oszczędności i miesięczną wpłatę. Oblicz, po ilu miesiącach uda się osiągnąć cel.

## 5. Suma cyfr liczby

Wczytaj liczbę całkowitą dodatnią. Oblicz sumę jej cyfr.

Podpowiedź:

- ostatnia cyfra to `liczba % 10`,
- usunięcie ostatniej cyfry to `liczba // 10`.

## 6. Odwrócenie liczby

Wczytaj liczbę całkowitą dodatnią i wypisz jej cyfry od końca.

Podpowiedź: użyj `% 10` oraz `// 10`.

## 7. Liczenie cyfr

Wczytaj liczbę całkowitą dodatnią i policz, ile ma cyfr.

## 8. Największa liczba z podanych

Wczytaj `n`. Następnie wczytaj `n` liczb i znajdź największą z nich.

Nie używaj list.

Podpowiedź: pierwszą wczytaną liczbę możesz zapisać jako aktualne maksimum.

## 9. Najmniejsza liczba z podanych

Wczytaj `n`. Następnie wczytaj `n` liczb i znajdź najmniejszą z nich.

Nie używaj list.

## 10. Statystyka ocen

Wczytaj `n` ocen. Oblicz:

- sumę ocen,
- średnią,
- liczbę ocen co najmniej `4`.

Nie używaj list.

## Kryteria oceny

Na ocenę dopuszczającą / dostateczną:

- poprawnie wykonane zadania proste,
- poprawne użycie pętli `for` albo `while`,
- programy uruchamiają się bez błędów,
- wyniki są czytelnie wypisane.

Na ocenę dobrą:

- wykonane zadania proste i kilka średnich,
- poprawne użycie licznika i akumulatora,
- brak pętli nieskończonych,
- czytelne nazwy zmiennych,
- sprawdzenie kilku różnych danych testowych.

Na ocenę bardzo dobrą:

- wykonane zadania trochę trudniejsze,
- poprawne użycie warunków w pętlach,
- poprawna obsługa przypadków granicznych,
- brak list tam, gdzie zadanie wymaga pracy bez list,
- samodzielne rozszerzenie przynajmniej jednego zadania.

## Typowe błędy

1. Brak zmiany licznika w pętli `while`.
2. Pętla nieskończona.
3. Brak dwukropka po `while` albo `for`.
4. Brak wcięć.
5. Mylenie `range(5)` z liczbami od `1` do `5`.
6. Zapomnienie o `n + 1` w `range(1, n + 1)`.
7. Ustawienie iloczynu na `0` zamiast na `1`.
8. Wypisanie wyniku końcowego wewnątrz pętli zamiast po pętli.
9. Mylenie licznika z akumulatorem.
10. Używanie list mimo zakazu.
11. Użycie `break`, mimo że zadanie wymaga rozwiązania przez warunek pętli.
12. Brak konwersji `int()` albo `float()` przy `input()`.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania w swoim folderze w JupyterLab.

Każde zadanie powinno być zapisane w osobnym pliku `.py` albo wyraźnie oddzielone w notebooku.

Proponowane nazwy plików:

```text
petle_a01.py
petle_a02.py
petle_b01.py
petle_c01.py
```
