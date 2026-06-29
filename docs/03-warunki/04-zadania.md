# Zadania - instrukcje warunkowe if, else i elif

## Cel lekcji

Utrwalisz instrukcje warunkowe `if`, `else` i `elif` w praktycznych zadaniach.

To jest lekcja ćwiczeniowa. Nie poznajesz tu nowej teorii, tylko używasz warunków w różnych sytuacjach.

## Czego używasz w tej lekcji

W zadaniach możesz używać:

- `print()`,
- zmiennych,
- `input()`,
- `int()`,
- `float()`,
- `str()`,
- operatorów arytmetycznych,
- operatorów porównania,
- `if`,
- `else`,
- `elif`,
- operatora `%`,
- prostych obliczeń.

Nie używaj jeszcze pętli, list, funkcji własnych, klas ani bibliotek zewnętrznych.

## Krótkie przypomnienie

- `if` wykonuje kod, gdy warunek jest prawdziwy.
- `else` wykonuje kod, gdy warunek z `if` jest fałszywy.
- `elif` pozwala sprawdzić kolejny warunek.
- `else` nie ma własnego warunku.
- Po `if`, `elif` i `else` stawiamy dwukropek.
- Kod należący do warunku musi być wcięty.
- Operator `==` służy do porównania.
- Operator `=` służy do przypisania.
- Operator `%` pozwala sprawdzić resztę z dzielenia.

## Zasady wykonywania zadań

1. Każde zadanie zapisz w osobnym pliku albo wyraźnie oddziel w notebooku.
2. Program ma pytać użytkownika o dane, jeżeli zadanie tego wymaga.
3. Program ma wypisywać czytelny wynik, nie samą liczbę.
4. Używaj czytelnych nazw zmiennych.
5. Stosuj `if`, `else` i `elif` tylko tam, gdzie są potrzebne.
6. Nie używaj jeszcze pętli.
7. Testuj program dla różnych danych.
8. Sprawdzaj przypadki graniczne, na przykład `0`, `18`, `50`, `100`.

Zadania są podzielone na poziomy. Nie każdy uczeń musi wykonać wszystkie zadania. Zadania proste sprawdzają podstawy. Zadania średnie wymagają połączenia kilku warunków. Zadania trochę trudniejsze są dla osób, które chcą powalczyć o wyższą ocenę.

# A. Zadania proste

Zadania proste sprawdzają, czy umiesz zapisać prosty warunek i wypisać odpowiedni komunikat.

## 1. Liczba dodatnia

Wczytaj liczbę i sprawdź, czy jest większa od zera.

## 2. Pełnoletność

Wczytaj wiek użytkownika i sprawdź, czy ma co najmniej `18` lat.

## 3. Hasło

Wczytaj hasło i sprawdź, czy jest równe `"python"`.

## 4. Liczba parzysta

Wczytaj liczbę i sprawdź, czy jest parzysta.

## 5. Temperatura

Wczytaj temperaturę i sprawdź, czy jest większa niż `30` stopni.

## 6. Punkty z testu

Wczytaj liczbę punktów i sprawdź, czy uczeń zaliczył test. Za zaliczenie przyjmij co najmniej `50` punktów.

## 7. Cena produktu

Wczytaj cenę produktu i sprawdź, czy jest większa niż `100` zł.

## 8. Liczba równa zero

Wczytaj liczbę i sprawdź, czy jest równa zero.

## 9. Imię

Wczytaj imię i sprawdź, czy użytkownik coś wpisał.

## 10. Wzrost

Wczytaj wzrost w centymetrach i sprawdź, czy jest większy niż `180`.

# B. Zadania średnie

Zadania średnie wymagają użycia `if-else` albo `if-elif-else`.

## 1. Dodatnia, ujemna czy zero

Wczytaj liczbę i wypisz, czy jest dodatnia, ujemna czy równa zero.

## 2. Parzysta czy nieparzysta

Wczytaj liczbę i wypisz, czy jest parzysta czy nieparzysta.

## 3. Ocena z punktów

Wczytaj liczbę punktów i wypisz:

- `bardzo dobry`, gdy punktów jest co najmniej `90`,
- `dobry`, gdy punktów jest co najmniej `75`,
- `dostateczny`, gdy punktów jest co najmniej `50`,
- `brak zaliczenia`, gdy punktów jest mniej niż `50`.

## 4. Temperatura opisowo

Wczytaj temperaturę i wypisz:

- `gorąco`, gdy temperatura jest większa niż `30`,
- `ciepło`, gdy jest większa niż `20`,
- `chłodno`, gdy jest większa niż `10`,
- `zimno`, w pozostałych przypadkach.

## 5. Menu programu

Wczytaj numer opcji:

```text
1 - start
2 - ustawienia
3 - koniec
```

Dla każdej opcji wypisz odpowiedni komunikat. Dla innej liczby wypisz `Nieznana opcja`.

## 6. Dzień tygodnia

Wczytaj numer dnia od `1` do `7` i wypisz nazwę dnia tygodnia. Dla błędnego numeru wypisz komunikat o błędzie.

## 7. Kategoria wieku

Wczytaj wiek i wypisz:

- `dziecko` dla wieku poniżej `13` lat,
- `nastolatek` dla wieku od `13` do `17` lat,
- `osoba dorosła` dla wieku od `18` do `64` lat,
- `senior` dla wieku od `65` lat.

## 8. Podzielność

Wczytaj liczbę i sprawdź, czy jest podzielna przez `3`, przez `5`, przez obie liczby albo przez żadną z nich.

## 9. Rabat

Wczytaj wartość zakupów. Jeżeli wartość jest większa niż `200` zł, nalicz rabat `10%`. W przeciwnym razie wypisz cenę bez rabatu.

## 10. Prosty kalkulator

Wczytaj dwie liczby i numer działania:

```text
1 - dodawanie
2 - odejmowanie
3 - mnożenie
4 - dzielenie
```

Wykonaj wybrane działanie.

# C. Zadania trochę trudniejsze

Te zadania wymagają uważniejszego myślenia o kolejności warunków, przypadkach granicznych i czytelnym wyniku.

## 1. Klasyfikacja wyniku sportowego

Wczytaj czas biegu na `100 m` i wypisz ocenę wyniku:

- poniżej `12` sekund - bardzo dobry wynik,
- od `12` do `15` sekund - dobry wynik,
- powyżej `15` sekund - wynik do poprawy.

## 2. Kalkulator biletu

Wczytaj wiek użytkownika i cenę biletu normalnego.

Zastosuj zniżki:

- dziecko do `7` lat - bilet za `0` zł,
- uczeń do `18` lat - `50%` ceny,
- senior od `65` lat - `30%` ceny,
- pozostali - pełna cena.

## 3. System oceniania

Wczytaj procentowy wynik testu i wypisz ocenę:

- `0-39%` - niedostateczny,
- `40-54%` - dopuszczający,
- `55-69%` - dostateczny,
- `70-84%` - dobry,
- `85-94%` - bardzo dobry,
- `95-100%` - celujący.

Dla wartości spoza zakresu `0-100` wypisz błąd danych.

## 4. Opłata za parking

Wczytaj liczbę godzin parkowania.

Zasady:

- pierwsza godzina: `4` zł,
- druga i trzecia godzina: `3` zł za godzinę,
- każda następna: `2` zł za godzinę.

Nie używaj pętli.

## 5. Koszt przesyłki

Wczytaj wagę paczki w kilogramach.

Ustal koszt:

- do `1 kg` - `12` zł,
- do `5 kg` - `18` zł,
- do `10 kg` - `25` zł,
- powyżej `10 kg` - `40` zł.

## 6. Bezpieczna prędkość

Wczytaj dozwoloną prędkość i prędkość pojazdu.

Oblicz przekroczenie i wypisz:

- brak mandatu,
- małe przekroczenie,
- średnie przekroczenie,
- duże przekroczenie.

Samodzielnie ustaw progi i wypisz je w programie.

## 7. Kalkulator BMI z podanym wzorem

Wczytaj masę w kilogramach i wzrost w metrach.

Oblicz BMI według wzoru:

```text
BMI = masa / (wzrost * wzrost)
```

Wypisz kategorię:

- poniżej `18.5` - niedowaga,
- `18.5-24.9` - norma,
- `25-29.9` - nadwaga,
- `30` i więcej - otyłość.

## 8. Decyzja o wycieczce

Wczytaj temperaturę i informację o opadach jako tekst `"tak"` albo `"nie"`.

Jeżeli temperatura jest co najmniej `18` i nie pada, wypisz, że można iść na wycieczkę. W przeciwnym razie wypisz, że wycieczkę lepiej przełożyć.

## 9. Ocena zakupów

Wczytaj kwotę zakupów.

Wypisz:

- małe zakupy,
- średnie zakupy,
- duże zakupy.

Dodatkowo, jeśli kwota przekracza `300` zł, nalicz rabat `15%`.

## 10. Logowanie

Wczytaj login i hasło.

Poprawne dane to:

```text
login: admin
hasło: python
```

Wypisz, czy logowanie się udało. Jeżeli login jest zły, wypisz `Nieznany użytkownik`. Jeżeli login jest dobry, ale hasło złe, wypisz `Błędne hasło`.

## Kryteria oceny

Na ocenę dopuszczającą / dostateczną:

- poprawnie wykonane zadania proste,
- poprawne użycie `if` albo `if-else`,
- programy uruchamiają się bez błędów,
- wyniki są czytelnie wypisane.

Na ocenę dobrą:

- wykonane zadania proste i kilka średnich,
- poprawne użycie `if-elif-else`,
- poprawna kolejność warunków,
- czytelne nazwy zmiennych,
- sprawdzenie kilku różnych danych testowych.

Na ocenę bardzo dobrą:

- wykonane zadania trochę trudniejsze,
- poprawna obsługa przypadków granicznych,
- czytelne komunikaty,
- samodzielne rozszerzenie przynajmniej jednego zadania,
- brak przypadkowych lub niepotrzebnych warunków.

## Typowe błędy

1. Mylenie `=` oraz `==`.
2. Brak dwukropka po `if`, `elif` albo `else`.
3. Brak wcięć.
4. Dopisywanie warunku po `else`.
5. Zła kolejność warunków.
6. Używanie kilku osobnych `if` zamiast `if-elif-else`.
7. Brak konwersji `int()` albo `float()`.
8. Porównywanie tekstu z liczbą.
9. Wypisywanie wyniku bez opisu.
10. Nieuwzględnienie przypadku granicznego, na przykład dokładnie `50` punktów.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania w swoim folderze w JupyterLab.

Każde zadanie powinno być zapisane w osobnym pliku `.py` albo wyraźnie oddzielone w notebooku.

Proponowane nazwy plików:

```text
warunki_a01.py
warunki_a02.py
warunki_b01.py
warunki_c01.py
```
