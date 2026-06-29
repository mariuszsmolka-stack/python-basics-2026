# Zadania - input(), print() i konwersja typów

## Cel lekcji

Utrwalisz wczytywanie danych od użytkownika, zamianę tekstu na liczby oraz wypisywanie czytelnych wyników.

To jest lekcja ćwiczeniowa. Nie poznajesz tu nowej teorii, tylko używasz tego, co już było na lekcjach.

## Czego używasz w tej lekcji

W zadaniach możesz używać:

- `print()`,
- zmiennych,
- `input()`,
- `int()`,
- `float()`,
- `str()`,
- operatorów arytmetycznych,
- prostych obliczeń.

F-stringi możesz używać jako opcję dla chętnych, zwłaszcza gdy chcesz ładnie sformatować wynik.

Nie używaj jeszcze instrukcji warunkowych, pętli, list, funkcji własnych, klas ani bibliotek zewnętrznych.

## Krótkie przypomnienie

- `input()` wczytuje dane jako tekst.
- `int()` zamienia tekst na liczbę całkowitą.
- `float()` zamienia tekst na liczbę rzeczywistą.
- `print()` wypisuje wynik na ekranie.
- Przecinki w `print()` oddzielają elementy do wypisania.
- W Pythonie liczby rzeczywiste zapisujemy z kropką, na przykład `3.5`.

## Zasady wykonywania zadań

1. Każde zadanie zapisz w osobnym pliku albo wyraźnie oddziel w notebooku.
2. Program ma pytać użytkownika o dane.
3. Program ma wypisywać czytelny wynik, nie samą liczbę.
4. Używaj czytelnych nazw zmiennych.
5. Nie używaj jeszcze instrukcji `if` ani pętli.
6. Testuj program dla różnych danych.
7. W zadaniach trochę trudniejszych możesz użyć f-stringów do ładnego formatowania wyniku.

Zadania są podzielone na poziomy. Nie każdy uczeń musi wykonać wszystkie zadania. Zadania proste sprawdzają podstawy. Zadania średnie wymagają połączenia kilku kroków. Zadania trochę trudniejsze są dla osób, które chcą powalczyć o wyższą ocenę.

# A. Zadania proste

Zadania proste sprawdzają, czy umiesz użyć `input()`, `print()` oraz podstawowej konwersji typów.

## 1. Powitanie

Wczytaj imię użytkownika i wypisz komunikat:

```text
Cześć, ...
```

## 2. Wizytówka

Wczytaj imię, nazwisko i klasę. Wypisz krótką wizytówkę ucznia.

## 3. Suma dwóch liczb

Wczytaj dwie liczby całkowite i wypisz ich sumę.

## 4. Różnica wieku

Wczytaj rok obecny i rok urodzenia. Oblicz przybliżony wiek.

## 5. Pole kwadratu

Wczytaj długość boku kwadratu i oblicz jego pole.

## 6. Pole prostokąta

Wczytaj długość i szerokość prostokąta. Oblicz jego pole.

## 7. Kilometry na metry

Wczytaj liczbę kilometrów i przelicz ją na metry.

## 8. Cena za kilka sztuk

Wczytaj cenę jednego produktu i liczbę sztuk. Oblicz koszt całkowity.

## 9. Średnia dwóch ocen

Wczytaj dwie oceny i oblicz ich średnią.

## 10. Minuty na sekundy

Wczytaj liczbę minut i przelicz ją na sekundy.

# B. Zadania średnie

Zadania średnie wymagają kilku obliczeń albo połączenia kilku danych w jednym programie.

## 1. Mały paragon

Wczytaj nazwę produktu, cenę jednej sztuki i liczbę sztuk. Wypisz prosty paragon z nazwą produktu i kwotą do zapłaty.

## 2. Cena brutto

Wczytaj cenę netto i stawkę VAT w procentach. Oblicz cenę brutto.

Wzór:

```python
cena_brutto = cena_netto + cena_netto * stawka_vat / 100
```

## 3. Przelicznik czasu

Wczytaj liczbę minut. Oblicz, ile to pełnych godzin i ile minut zostaje.

Podpowiedź: użyj `//` oraz `%`.

## 4. Koszt wycieczki

Wczytaj liczbę uczniów, koszt biletu dla jednej osoby i koszt transportu. Oblicz całkowity koszt wycieczki.

## 5. Średnia z trzech ocen

Wczytaj trzy oceny i oblicz średnią.

## 6. Dzienny plan czytania

Wczytaj liczbę stron książki i liczbę dni. Oblicz, ile stron trzeba czytać dziennie.

## 7. Prędkość średnia

Wczytaj dystans w kilometrach i czas w godzinach. Oblicz średnią prędkość.

## 8. Koszt paliwa

Wczytaj długość trasy w kilometrach, spalanie na 100 km i cenę litra paliwa. Oblicz koszt przejazdu.

Wzór:

```python
zuzycie_paliwa = dystans * spalanie / 100
koszt = zuzycie_paliwa * cena_litra
```

## 9. Wynagrodzenie za pracę

Wczytaj liczbę godzin pracy i stawkę za godzinę. Oblicz wynagrodzenie.

## 10. Prosty budżet

Wczytaj dochód, koszt jedzenia, koszt transportu i inne wydatki. Oblicz, ile pieniędzy zostaje.

# C. Zadania trochę trudniejsze

Te zadania są dla osób, które dobrze radzą sobie z podstawami i chcą zrobić coś bardziej rozbudowanego. Nadal nie używamy instrukcji warunkowych ani pętli.

## 1. Paragon z VAT i dostawą

Wczytaj nazwę produktu, cenę netto, liczbę sztuk, stawkę VAT i koszt dostawy. Oblicz:

- wartość netto,
- kwotę VAT,
- wartość brutto,
- końcową kwotę z dostawą.

## 2. Kalkulator rat

Wczytaj cenę produktu i liczbę rat. Oblicz wysokość jednej raty.

Dla chętnych: wypisz ratę z dwoma miejscami po kropce.

## 3. Zamówienie pizzy

Wczytaj cenę jednej pizzy, liczbę pizz, koszt dostawy i liczbę osób. Oblicz:

- całkowity koszt zamówienia,
- koszt na jedną osobę.

## 4. Remont pokoju

Wczytaj długość i szerokość pokoju oraz cenę paneli za metr kwadratowy. Oblicz:

- powierzchnię pokoju,
- koszt paneli.

## Kryteria oceny

Praca jest zaliczona, jeżeli:

- programy uruchamiają się bez błędów,
- programy pytają użytkownika o dane,
- dane liczbowe są poprawnie zamieniane przez `int()` albo `float()`,
- wyniki są opisane tekstem,
- nazwy zmiennych są czytelne,
- obliczenia są poprawne,
- zadania są zapisane w uporządkowany sposób.

Na wyższą ocenę warto wykonać zadania z poziomu B oraz przynajmniej jedno zadanie z poziomu C.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania w swoim folderze w JupyterLab.

Zadania mogą być zapisane w notebooku albo w osobnych plikach `.py`, zgodnie z poleceniem nauczyciela.
