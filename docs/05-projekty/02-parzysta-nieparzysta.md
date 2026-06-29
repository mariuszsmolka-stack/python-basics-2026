# Projekt - liczba parzysta, nieparzysta i podzielność

## Cel projektu

Celem projektu jest napisanie programu, który wczytuje jedną liczbę całkowitą i sprawdza jej podstawowe właściwości.

Projekt pozwala przećwiczyć `input()`, konwersję typów, operator `%`, instrukcje `if`, `if-else`, `elif` oraz komentarze.

## Co program ma robić

Program ma:

- zapytać użytkownika o liczbę całkowitą,
- sprawdzić, czy liczba jest parzysta czy nieparzysta,
- sprawdzić, czy liczba jest dodatnia, ujemna czy równa zero,
- sprawdzić, czy liczba jest podzielna przez `3`,
- sprawdzić, czy liczba jest podzielna przez `5`,
- wypisać czytelne podsumowanie.

Operator `%` zwraca resztę z dzielenia.

```python
liczba % 2 == 0
```

Ten warunek oznacza: liczba jest podzielna przez `2`, czyli jest parzysta.

## Wymagania funkcjonalne

Program powinien:

- wczytać liczbę całkowitą od użytkownika,
- użyć `int(input(...))`,
- sprawdzić parzystość liczby,
- sprawdzić znak liczby: dodatnia, ujemna albo zero,
- sprawdzić podzielność przez `3`,
- sprawdzić podzielność przez `5`,
- wypisać wynik w czytelnej formie,
- używać instrukcji `if`, `else` i `elif` tam, gdzie są potrzebne.

## Wymagania techniczne

W projekcie używamy:

- zmiennych,
- `print()`,
- `input()`,
- `int()`,
- operatora `%`,
- operatorów porównania,
- instrukcji `if`, `elif`, `else`,
- komentarzy.

W projekcie nie używamy:

- list,
- funkcji własnych,
- pętli,
- klas,
- plików,
- bibliotek zewnętrznych.

## Przykładowe działanie programu

```text
Projekt: analiza liczby

Podaj liczbę całkowitą: 15

Podsumowanie:
Liczba: 15
Liczba jest nieparzysta.
Liczba jest dodatnia.
Liczba jest podzielna przez 3.
Liczba jest podzielna przez 5.
```

## Wersja podstawowa

W wersji podstawowej program wczytuje jedną liczbę i sprawdza jej właściwości.

Przykładowe fragmenty warunków:

```python
if liczba % 2 == 0:
    print("Liczba jest parzysta.")
else:
    print("Liczba jest nieparzysta.")
```

```python
if liczba > 0:
    print("Liczba jest dodatnia.")
elif liczba < 0:
    print("Liczba jest ujemna.")
else:
    print("Liczba jest równa zero.")
```

## Etapy wykonania projektu

1. Utwórz plik projektu.
2. Wypisz tytuł programu.
3. Wczytaj liczbę całkowitą od użytkownika.
4. Sprawdź, czy liczba jest parzysta.
5. Sprawdź, czy liczba jest dodatnia, ujemna czy równa zero.
6. Sprawdź, czy liczba jest podzielna przez `3`.
7. Sprawdź, czy liczba jest podzielna przez `5`.
8. Wypisz czytelne podsumowanie.
9. Dodaj przynajmniej jeden sensowny komentarz.
10. Przetestuj program dla kilku liczb, na przykład `-6`, `0`, `4`, `9`, `10`, `15`.

## Podpowiedzi

Do wczytania liczby użyj `int(input(...))`.

Do sprawdzania parzystości użyj operatora `%`.

Liczba jest parzysta, gdy `liczba % 2 == 0`.

Liczba jest podzielna przez `3`, gdy `liczba % 3 == 0`.

Liczba jest podzielna przez `5`, gdy `liczba % 5 == 0`.

Do sprawdzenia znaku liczby użyj `if` / `elif` / `else`.

Wynik powinien być opisany tekstem, nie samą liczbą.

## Co uczeń ma dodać od siebie?

Uczeń ma dodać od siebie co najmniej 5 elementów, w tym co najmniej jedną zmianę wpływającą na działanie programu, a nie tylko na tekst komunikatów.

Sama zmiana tekstów i tytułu programu nie wystarczy. Przynajmniej jedna zmiana musi wpływać na logikę programu.

Możliwe dodatki:

1. Własny tytuł programu.
2. Własne komunikaty dla użytkownika.
3. Dodatkowe sprawdzenie podzielności przez `4`.
4. Dodatkowe sprawdzenie podzielności przez `10`.
5. Informację, jaka jest reszta z dzielenia przez `2`.
6. Informację, jaka jest reszta z dzielenia przez `3`.
7. Dodatkową klasyfikację: liczba mała, średnia albo duża.
8. Czytelniejsze podsumowanie z pustymi liniami.
9. Przynajmniej jeden komentarz wyjaśniający użycie operatora `%`.
10. Własne nazwy zmiennych, które są czytelne i pasują do programu.

## Przykłady zmian, które możesz dodać

1. Podzielność przez 10

Program sprawdza, czy liczba jest podzielna przez `10`.

2. Klasyfikacja wielkości liczby

Program wypisuje:

- `Liczba mała`, gdy liczba jest mniejsza niż `10`,
- `Liczba średnia`, gdy liczba jest od `10` do `99`,
- `Liczba duża`, gdy liczba ma co najmniej `100`.

3. Reszta z dzielenia

Program wypisuje resztę z dzielenia przez `2` i przez `3`.

4. Dodatkowy komunikat końcowy

Program kończy działanie komunikatem:

```text
Dziękuję za użycie programu.
```

5. Ładniejsze podsumowanie

Program wypisuje nagłówek:

```text
--- PODSUMOWANIE ANALIZY LICZBY ---
```

## Przykładowy zestaw zmian dla ucznia

Uczeń może wybrać na przykład taki zestaw 5 zmian:

1. Zmienić tytuł programu.
2. Dodać sprawdzanie podzielności przez `10`.
3. Dodać wypisanie reszty z dzielenia przez `3`.
4. Dodać klasyfikację liczby jako mała, średnia albo duża.
5. Dodać czytelne podsumowanie z nagłówkiem.

Drugi przykładowy zestaw:

1. Zmienić komunikaty dla użytkownika.
2. Dodać sprawdzanie podzielności przez `4`.
3. Dodać informację o reszcie z dzielenia przez `2`.
4. Dodać komentarz wyjaśniający operator `%`.
5. Dodać komunikat końcowy.

## Kryteria zaliczenia

Program jest zaliczony, jeżeli:

- uruchamia się bez błędów,
- wczytuje liczbę od użytkownika,
- używa `int(input(...))`,
- poprawnie sprawdza parzystość,
- poprawnie sprawdza, czy liczba jest dodatnia, ujemna czy równa zero,
- poprawnie sprawdza podzielność przez `3`,
- poprawnie sprawdza podzielność przez `5`,
- wypisuje czytelne podsumowanie,
- używa poprawnych nazw zmiennych,
- zawiera przynajmniej jeden sensowny komentarz,
- zawiera minimum 5 samodzielnych zmian, w tym jedną zmianę logiczną.

## Typowe błędy uczniów

1. Brak `int()` przy `input()`.
2. Mylenie `/` oraz `%`.
3. Mylenie `=` oraz `==`.
4. Brak dwukropka po `if`, `elif` albo `else`.
5. Brak wcięć.
6. Użycie kilku `if` tam, gdzie potrzebne jest `if` / `elif` / `else`.
7. Niewłaściwe sprawdzanie parzystości.
8. Wypisanie wyniku bez opisu.
9. Zbyt krótkie lub nieczytelne nazwy zmiennych.
10. Brak samodzielnych zmian w projekcie.

## Czego nie robić

Nie używaj list, funkcji własnych ani pętli.

Nie wypisuj samego wyniku bez opisu.

Nie kopiuj programu bez zrozumienia.

Nie używaj nazw zmiennych `x`, `y`, `z`, jeśli można użyć czytelniejszych nazw.

## Sposób oddania pracy

Uczeń zapisuje projekt w swoim folderze w JupyterLab.

Nazwa pliku:

```text
projekt_02_parzysta_nieparzysta.py
```

Uczeń może najpierw testować rozwiązanie w notebooku, ale ostateczna wersja powinna być zapisana jako plik `.py`.
