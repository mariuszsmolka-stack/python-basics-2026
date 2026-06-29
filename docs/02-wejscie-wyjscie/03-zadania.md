# Zadania — input(), print() i konwersja typów

## Cel lekcji

Celem lekcji jest utrwalenie wczytywania danych od użytkownika, zamiany tekstu na liczby oraz wypisywania czytelnych wyników.

To jest lekcja ćwiczeniowa. Nie poznajesz tu nowej teorii. Ćwiczysz to, co było już na lekcjach o `print()`, `input()` i konwersji typów.

## Krótkie przypomnienie

`input()` wczytuje dane od użytkownika jako tekst, czyli typ `str`.

Jeżeli chcesz wykonać obliczenia na liczbach całkowitych, użyj `int()`.

Jeżeli chcesz wykonać obliczenia na liczbach rzeczywistych, użyj `float()`.

Do wypisywania wyników używamy `print()`.

Przykład:

```python
cena = float(input("Podaj cenę: "))
liczba_sztuk = int(input("Podaj liczbę sztuk: "))
koszt = cena * liczba_sztuk

print("Koszt wynosi:", koszt)
```

W tej lekcji możesz używać:

1. `print()`,
2. zmiennych,
3. `input()`,
4. `int()`,
5. `float()`,
6. `str()`,
7. operatorów arytmetycznych,
8. prostych obliczeń.

F-stringi są tylko opcją dla chętnych. Możesz ich użyć, gdy chcesz ładnie sformatować wynik.

Nie używaj jeszcze:

1. `if`, `elif`, `else`,
2. `while`,
3. `for`,
4. list,
5. funkcji własnych,
6. klas,
7. bibliotek zewnętrznych.

## Zasady wykonywania zadań

1. Każde zadanie zapisz w osobnym pliku albo wyraźnie oddziel w notebooku.
2. Program ma pytać użytkownika o dane.
3. Program ma wypisywać czytelny wynik, nie samą liczbę.
4. Używaj czytelnych nazw zmiennych.
5. Liczby całkowite zamieniaj za pomocą `int()`.
6. Liczby rzeczywiste zamieniaj za pomocą `float()`.
7. Testuj program dla różnych danych.
8. Nie każdy uczeń musi wykonać wszystkie zadania.

Poziomy:

1. A — poziom podstawowy,
2. B — poziom dobry,
3. C — poziom dla uczniów celujących w wyższą ocenę.

## A. Zadania proste

### 1. Powitanie

Wczytaj imię użytkownika i wypisz powitanie.

Przykład wyniku:

```text
Cześć, Ania!
```

### 2. Wizytówka

Wczytaj imię, nazwisko i klasę. Wypisz krótką wizytówkę ucznia.

### 3. Suma dwóch liczb

Wczytaj dwie liczby całkowite i wypisz ich sumę.

### 4. Pole kwadratu

Wczytaj długość boku kwadratu i oblicz jego pole.

### 5. Pole prostokąta

Wczytaj długość i szerokość prostokąta. Oblicz jego pole.

### 6. Kilometry na metry

Wczytaj liczbę kilometrów i przelicz ją na metry.

Podpowiedź:

```python
metry = kilometry * 1000
```

### 7. Cena za kilka sztuk

Wczytaj cenę jednego produktu i liczbę sztuk. Oblicz koszt całkowity.

### 8. Średnia dwóch ocen

Wczytaj dwie oceny i oblicz ich średnią.

### 9. Minuty na sekundy

Wczytaj liczbę minut i przelicz ją na sekundy.

### 10. Rok urodzenia

Wczytaj rok obecny i rok urodzenia. Oblicz przybliżony wiek użytkownika.

## B. Zadania średnie

### 1. Mały paragon

Wczytaj nazwę produktu, cenę jednej sztuki i liczbę sztuk. Wypisz prosty paragon z nazwą produktu i kwotą do zapłaty.

### 2. Cena brutto

Wczytaj cenę netto i stawkę VAT w procentach. Oblicz cenę brutto.

Wzór:

```python
cena_brutto = cena_netto + cena_netto * stawka_vat / 100
```

### 3. Przelicznik czasu z // i %

Wczytaj liczbę minut. Oblicz, ile to pełnych godzin i ile minut zostaje.

Podpowiedź:

```python
godziny = minuty // 60
pozostale_minuty = minuty % 60
```

### 4. Koszt wycieczki

Wczytaj liczbę uczniów, koszt biletu dla jednej osoby i koszt transportu. Oblicz całkowity koszt wycieczki.

### 5. Średnia z trzech ocen

Wczytaj trzy oceny i oblicz ich średnią.

### 6. Dzienny plan czytania

Wczytaj liczbę stron książki i liczbę dni. Oblicz, ile stron trzeba czytać dziennie.

### 7. Prędkość średnia

Wczytaj dystans w kilometrach i czas w godzinach. Oblicz średnią prędkość.

Wzór:

```python
predkosc = dystans / czas
```

### 8. Koszt paliwa

Wczytaj długość trasy w kilometrach, spalanie na 100 km i cenę litra paliwa. Oblicz koszt przejazdu.

Wzór:

```python
zuzycie_paliwa = dystans * spalanie / 100
koszt = zuzycie_paliwa * cena_litra
```

### 9. Wynagrodzenie

Wczytaj liczbę godzin pracy i stawkę za godzinę. Oblicz wynagrodzenie.

### 10. Prosty budżet

Wczytaj dochód, koszt jedzenia, koszt transportu i inne wydatki. Oblicz, ile pieniędzy zostaje.

## C. Zadania trochę trudniejsze

Te zadania są nadal bez instrukcji warunkowych i bez pętli. Są dłuższe, bo wymagają kilku danych i kilku obliczeń.

### 1. Paragon z VAT i dostawą

Wczytaj nazwę produktu, cenę netto, liczbę sztuk, stawkę VAT i koszt dostawy. Oblicz wartość netto, kwotę VAT, wartość brutto oraz końcową kwotę z dostawą.

### 2. Kalkulator rat

Wczytaj cenę produktu i liczbę rat. Oblicz wysokość jednej raty.

Dla chętnych: wypisz ratę z dwoma miejscami po kropce.

### 3. Zamówienie pizzy

Wczytaj cenę jednej pizzy, liczbę pizz, koszt dostawy i liczbę osób. Oblicz całkowity koszt zamówienia oraz koszt na jedną osobę.

### 4. Remont pokoju

Wczytaj długość i szerokość pokoju oraz cenę paneli za metr kwadratowy. Oblicz powierzchnię pokoju i koszt paneli.

### 5. Koszt przejazdu

Wczytaj długość trasy, spalanie samochodu, cenę paliwa oraz liczbę osób. Oblicz koszt paliwa i koszt przejazdu na jedną osobę.

### 6. Plan oszczędzania

Wczytaj kwotę, którą chcesz uzbierać, oraz kwotę odkładaną co miesiąc. Oblicz, ile miesięcy potrzeba w prostym obliczeniu dzielenia.

Nie używaj jeszcze zaokrąglania warunkowego. Wynik może być liczbą rzeczywistą.

### 7. Sekundy na godziny, minuty i sekundy

Wczytaj liczbę sekund. Oblicz, ile to pełnych godzin, ile pełnych minut zostaje i ile sekund zostaje.

Podpowiedź:

```python
godziny = sekundy // 3600
reszta = sekundy % 3600
minuty = reszta // 60
pozostale_sekundy = reszta % 60
```

### 8. Koszt druku

Wczytaj liczbę stron czarno-białych, liczbę stron kolorowych, cenę jednej strony czarno-białej i cenę jednej strony kolorowej. Oblicz całkowity koszt druku.

### 9. Organizacja klasowej składki

Wczytaj liczbę uczniów, kwotę składki od jednej osoby i koszt planowanego zakupu. Oblicz zebraną kwotę oraz różnicę między zebraną kwotą a kosztem zakupu.

### 10. Prosty kalkulator budżetu miesięcznego

Wczytaj miesięczny dochód oraz kilka wydatków: jedzenie, transport, telefon, rozrywkę i inne koszty. Oblicz łączną kwotę wydatków i kwotę, która zostaje.

## Kryteria oceny

Praca jest zaliczona, jeżeli:

1. programy uruchamiają się bez błędów,
2. programy pytają użytkownika o dane,
3. dane liczbowe są poprawnie zamieniane przez `int()` albo `float()`,
4. wyniki są opisane tekstem,
5. nazwy zmiennych są czytelne,
6. obliczenia są poprawne,
7. zadania są zapisane w uporządkowany sposób.

Na poziom podstawowy wykonaj zadania z części A.

Na poziom dobry wykonaj zadania z części A oraz wybrane zadania z części B.

Na wyższą ocenę wykonaj także wybrane zadania z części C.

## Typowe błędy

1. Brak `int()` albo `float()` przy danych liczbowych z `input()`.
2. Próba dodawania tekstów zamiast liczb.
3. Wpisanie przecinka zamiast kropki w liczbie rzeczywistej, na przykład `3,5` zamiast `3.5`.
4. Wypisanie samego wyniku bez opisu.
5. Używanie nieczytelnych nazw zmiennych.
6. Mylenie `//` oraz `/`.
7. Mylenie `%` z dzieleniem.
8. Brak nawiasów w obliczaniu średniej.
9. Zapomnienie, że `input()` zawsze zwraca tekst.
10. Używanie instrukcji `if`, pętli albo list, chociaż nie są jeszcze potrzebne w tej lekcji.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania w swoim folderze w JupyterLab.

Zadania mogą być zapisane w notebooku albo w osobnych plikach `.py`, zgodnie z poleceniem nauczyciela.

Proponowane nazwy plików:

```text
zadania_input_a01.py
zadania_input_b01.py
zadania_input_c01.py
```
