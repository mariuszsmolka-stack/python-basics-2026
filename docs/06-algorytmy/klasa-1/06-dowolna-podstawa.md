---
layout: default
title: Konwersje dla innych podstaw
---

# Konwersje dla innych podstaw

## Cel lekcji

Uogólnisz poznane dwa algorytmy. Zamiast stałej `2` użyjesz zmiennej `podstawa`. Podstawowe programy obsługują podstawy od `2` do `10`. Na końcu znajduje się rozszerzenie szesnastkowe dla chętnych.

## Co oznacza podstawa?

Podstawa określa liczbę dostępnych cyfr i wartości kolejnych pozycji. W systemie trójkowym cyfry to `0`, `1`, `2`. Cyfra `3` już nie jest dozwolona. W systemie o podstawie `8` dozwolone cyfry mają wartości od `0` do `7`.

Wartości pozycji rosną przez kolejne mnożenie przez podstawę. Nie potrzebujemy nowego pomysłu na algorytm. Zmieniamy liczbę używaną przy dzieleniu lub mnożeniu.

W miejscach, w których czytamy przez `int(input())`, zakładamy poprawnie wpisaną liczbę całkowitą. Sprawdzamy jej zakres. Napisy cyfr sprawdzamy znak po znaku. Nie obsługujemy znaków minus, spacji ani pustego napisu jako zapisu liczby.

## Etap A. Dziesiętny na podstawę od 2 do 10

### Przykład ręczny: 25 dziesiętnie => 221 trójkowo

| Liczba | Dzielenie z resztą | Iloraz | Reszta |
| --- | --- | --- | --- |
| 25 | 25 = 8 * 3 + 1 | 8 | 1 |
| 8 | 8 = 2 * 3 + 2 | 2 | 2 |
| 2 | 2 = 0 * 3 + 2 | 0 | 2 |

Reszty od końca => `221`. Każda reszta jest mniejsza od `3`, więc jest poprawną cyfrą trójkową.

### Algorytm i implementacja

Dziel liczbę całkowicie przez podstawę, odczytuj resztę i dopisuj jej znak na początku wyniku. Powtarzaj do otrzymania zera. Samo zero zapisz jako `"0"`. Liczbę ujemną i podstawę spoza zakresu odrzuć.

Dane przykładowe, w osobnych wierszach: `25`, potem `3`.

<details markdown="1">
<summary>Pokaż implementację A - zapis w podstawie 2-10</summary>

```python
liczba = int(input())
podstawa = int(input())
if liczba < 0 or podstawa < 2 or podstawa > 10:
    print("Błąd danych")
else:
    pozostalaLiczba = liczba
    wynik = ""
    if pozostalaLiczba == 0:
        wynik = "0"
    while pozostalaLiczba > 0:
        reszta = pozostalaLiczba % podstawa
        wynik = str(reszta) + wynik
        pozostalaLiczba = pozostalaLiczba // podstawa
    print(wynik)
```

Wynik:

```text
221
```

</details>

To program dla podstaw `2-10`, a nie dla wszystkich podstaw. W tym zakresie reszta jest jedną cyfrą dziesiętną, więc `str(reszta)` daje właściwy pojedynczy znak. Podstawa `1` nie jest dozwolona. Dzielenie przez nią nie zmniejszałoby dodatniej liczby w pętli.

## Etap B. Podstawa od 2 do 10 na dziesiętny

### Przykład ręczny: 221 trójkowo => 25 dziesiętnie

Wartości pozycji od prawej to `1`, `3`, `9`. Mamy `2 * 9 + 2 * 3 + 1 * 1 = 25`.

Ten sam wynik dostaniemy, przetwarzając cyfry od lewej:

| Cyfra | Obliczenie | Wynik |
| --- | --- | --- |
| 2 | 0 * 3 + 2 | 2 |
| 2 | 2 * 3 + 2 | 8 |
| 1 | 8 * 3 + 1 | 25 |

### Algorytm i implementacja

Najpierw sprawdź zakres podstawy, niepusty zapis i poprawność wszystkich cyfr. Każda cyfra musi być mniejsza od podstawy. Następnie dla każdej cyfry zastosuj `wynik = wynik * podstawa + cyfra`.

Dane przykładowe: `3` w pierwszym wierszu, `221` w drugim.

<details markdown="1">
<summary>Pokaż implementację B - wartość dziesiętna</summary>

```python
podstawa = int(input())
zapisLiczby = input()
czyPoprawny = podstawa >= 2 and podstawa <= 10 and len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
    else:
        cyfra = int(znak)
        if cyfra >= podstawa:
            czyPoprawny = False
if czyPoprawny:
    wynik = 0
    for znak in zapisLiczby:
        wynik = wynik * podstawa + int(znak)
    print(wynik)
else:
    print("Błąd danych")
```

Wynik:

```text
25
```

</details>

Sprawdzamy dwie różne rzeczy. Znak `A` nie jest cyfrą używaną w tej wersji programu. Znak `3` jest cyfrą dziesiętną, lecz nie jest poprawny w podstawie `3`. Oba błędy odrzucamy.

## Etap C. Konwersja między dwoma systemami

System źródłowy => system dziesiętny => system docelowy.

Przykład: `221` trójkowo => `25` dziesiętnie => `11001` dwójkowo.

Najpierw wykorzystujemy etap B z podstawą źródłową. Potem etap A z podstawą docelową. Wartość dziesiętna jest zwykłą liczbą typu `int`, a nie kolejnym napisem do ręcznego analizowania.

Dane w trzech wierszach: podstawa źródłowa `3`, podstawa docelowa `2`, zapis `221`. Obie podstawy muszą należeć do zakresu `2-10`.

<details markdown="1">
<summary>Pokaż implementację C - dwa etapy</summary>

```python
podstawaZrodlowa = int(input())
podstawaDocelowa = int(input())
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
if podstawaZrodlowa < 2 or podstawaZrodlowa > 10:
    czyPoprawny = False
if podstawaDocelowa < 2 or podstawaDocelowa > 10:
    czyPoprawny = False
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
    else:
        if int(znak) >= podstawaZrodlowa:
            czyPoprawny = False
if czyPoprawny:
    wartoscDziesietna = 0
    for znak in zapisLiczby:
        wartoscDziesietna = wartoscDziesietna * podstawaZrodlowa + int(znak)
    pozostalaLiczba = wartoscDziesietna
    wynik = ""
    if pozostalaLiczba == 0:
        wynik = "0"
    while pozostalaLiczba > 0:
        reszta = pozostalaLiczba % podstawaDocelowa
        wynik = str(reszta) + wynik
        pozostalaLiczba = pozostalaLiczba // podstawaDocelowa
    print(wynik)
else:
    print("Błąd danych")
```

Wynik:

```text
11001
```

</details>

Najpierw kończymy kontrolę danych. Potem pierwsza pętla oblicza wartość, a druga buduje nowy zapis. Zero dostaje zapis `0` także wtedy, gdy źródło miało kilka zer wiodących. Nie zachowujemy ich liczby podczas konwersji wartości.

## Etap D. System szesnastkowy - dla chętnych

W podstawie `16` potrzeba szesnastu cyfr. Po `0-9` używamy znaków `A`, `B`, `C`, `D`, `E`, `F`.

| Znak | A | B | C | D | E | F |
| --- | --- | --- | --- | --- | --- | --- |
| Wartość | 10 | 11 | 12 | 13 | 14 | 15 |

Przykład ręczny:

| Liczba | Iloraz przez 16 | Reszta | Znak reszty |
| --- | --- | --- | --- |
| 255 | 15 | 15 | F |
| 15 | 0 | 15 | F |

`255` dziesiętnie => `FF` szesnastkowo. W drugą stronę: `15 * 16 + 15 = 255`.

Nie wolno po prostu sklejać napisów `"15"` i `"15"`. Reszta `15` ma być **jedną cyfrą**, czyli znakiem `F`.

W ćwiczeniach dodatkowych użyjemy napisu `alfabet = "0123456789ABCDEF"`. `alfabet[15]` wybiera znak `F`, podobnie jak indeks wybiera element listy. Metoda napisu `alfabet.index(znak)` zwraca pozycję znaku, czyli w tym alfabecie jego wartość. Zanim jej użyjemy, sprawdzamy, czy znak występuje w alfabecie. W przeciwnym razie metoda zgłosiłaby `ValueError`.

Rozszerzenie przyjmuje duże litery `A-F`. Małe litery odrzuca. Dla podstaw mniejszych od `16` dodatkowo sprawdzamy, czy wartość cyfry jest mniejsza od podstawy. Znak `F` nie jest dozwolony na przykład w podstawie `10`.

Możliwe jest dalsze rozszerzenie alfabetu o pozostałe litery, aby obsługiwać podstawy do `36`. Nie jest ono częścią tych programów. Nie musisz jeszcze opanować rozszerzenia szesnastkowego.

## Typowe błędy

- Zmiana podstawy tylko przy dzieleniu albo tylko przy obliczaniu reszty.
- Przyjęcie, że cyfra równa podstawie jest dozwolona.
- Dopuszczenie podstawy `1`, `0` lub ujemnej.
- Używanie podstawy docelowej przy odczytywaniu źródła.
- Traktowanie dwucyfrowej wartości reszty `15` jak jednego zwykłego znaku dziesiętnego.
- Nazywanie wersji dla podstaw `2-10` konwerterem wszystkich systemów.

## Ćwiczenia podstawowe

### Ćwiczenie 1. Dziewiętnaście trójkowo

Przelicz ręcznie `19` dziesiętnie na system trójkowy, a potem sprawdź wynik własnym programem.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Każda reszta musi należeć do zbioru cyfr trójkowych. Najpierw zapisz ilorazy i reszty, potem ustal kierunek odczytu.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

Dzielenia: `19 = 6 * 3 + 1`, `6 = 2 * 3 + 0`, `2 = 0 * 3 + 2`. Wynik: `201`.

```python
liczba = 19
podstawa = 3
wynik = ""
while liczba > 0:
    wynik = str(liczba % podstawa) + wynik
    liczba = liczba // podstawa
print(wynik)
```

Wynik:

```text
201
```

To sprawdzenie konkretnego, dodatniego przykładu. Ogólny program z etapu A dodatkowo kontroluje dane i obsługuje zero.

</details>

### Ćwiczenie 2. Odczytaj zapis trójkowy

Wczytaj podstawę i zapis. Dla podstaw od `2` do `10` wypisz wartość dziesiętną. Odrzuć dane spoza zakresu i niepoprawne cyfry. Sprawdź podstawę `3` i zapis `102`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Przesuwanie dotychczasowych cyfr wymaga mnożenia przez podstawę, a nie zawsze przez dwa.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
podstawa = int(input())
zapisLiczby = input()
czyPoprawny = podstawa >= 2 and podstawa <= 10 and len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
    else:
        if int(znak) >= podstawa:
            czyPoprawny = False
if czyPoprawny:
    wynik = 0
    for znak in zapisLiczby:
        wynik = wynik * podstawa + int(znak)
    print(wynik)
else:
    print("Błąd danych")
```

Dla danych `3` i `102` wynik:

```text
11
```

</details>

### Ćwiczenie 3. Nieprawidłowa cyfra

Dla podstaw od `2` do `10` sprawdź, czy napis jest poprawny. Wypisz `Poprawny zapis` albo `Błąd danych`. Sprawdź cyfrę `3` w podstawie `3`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Sama obecność znaku wśród cyfr dziesiętnych nie wystarcza. Liczy się również jego wartość względem podstawy.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
podstawa = int(input())
zapisLiczby = input()
czyPoprawny = podstawa >= 2 and podstawa <= 10 and len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
    else:
        if int(znak) >= podstawa:
            czyPoprawny = False
if czyPoprawny:
    print("Poprawny zapis")
else:
    print("Błąd danych")
```

Dla danych `3` i `3` wynik:

```text
Błąd danych
```

</details>

### Ćwiczenie 4. Podstawa spoza zakresu

Napisz program konwersji liczby dziesiętnej na podstawę `2-10`. Sprawdź liczbę `10` i podstawę `1`. Program ma odrzucić dane, zamiast wejść w nieskończoną pętlę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Zakres podstawy trzeba sprawdzić przed pętlą. Nie każde dzielenie gwarantuje zmniejszanie liczby.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
liczba = int(input())
podstawa = int(input())
if liczba < 0 or podstawa < 2 or podstawa > 10:
    print("Błąd danych")
else:
    wynik = ""
    pozostalaLiczba = liczba
    if pozostalaLiczba == 0:
        wynik = "0"
    while pozostalaLiczba > 0:
        wynik = str(pozostalaLiczba % podstawa) + wynik
        pozostalaLiczba = pozostalaLiczba // podstawa
    print(wynik)
```

Dla danych `10` i `1` wynik:

```text
Błąd danych
```

</details>

### Ćwiczenie 5. Między systemami

Przelicz zapis z jednej podstawy `2-10` do innej podstawy `2-10` przez wartość dziesiętną. Wczytaj podstawę źródłową, docelową i napis. Sprawdź dane `2`, `3`, `1011`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Dwa znane etapy mają różne role. Wynik liczbowy pierwszego etapu jest wejściem do budowania napisu w drugim etapie.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
podstawaZrodlowa = int(input())
podstawaDocelowa = int(input())
zapisLiczby = input()
czyPoprawny = len(zapisLiczby) > 0
if podstawaZrodlowa < 2 or podstawaZrodlowa > 10:
    czyPoprawny = False
if podstawaDocelowa < 2 or podstawaDocelowa > 10:
    czyPoprawny = False
for znak in zapisLiczby:
    if znak not in "0123456789":
        czyPoprawny = False
    else:
        if int(znak) >= podstawaZrodlowa:
            czyPoprawny = False
if czyPoprawny:
    wartoscDziesietna = 0
    for znak in zapisLiczby:
        wartoscDziesietna = wartoscDziesietna * podstawaZrodlowa + int(znak)
    pozostalaLiczba = wartoscDziesietna
    wynik = ""
    if pozostalaLiczba == 0:
        wynik = "0"
    while pozostalaLiczba > 0:
        wynik = str(pozostalaLiczba % podstawaDocelowa) + wynik
        pozostalaLiczba = pozostalaLiczba // podstawaDocelowa
    print(wynik)
else:
    print("Błąd danych")
```

Dla danych `2`, `3`, `1011` wynik:

```text
102
```

</details>

## Ćwiczenia dodatkowe dla chętnych

### Ćwiczenie 6. Zapis szesnastkowy

Wczytaj nieujemną liczbę dziesiętną i zapisz ją szesnastkowo z dużymi literami. Użyj algorytmu dzielenia przez `16` i alfabetu cyfr. Sprawdź `255` i `0`. Liczbę ujemną odrzuć.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 6</summary>

Reszta jest wartością cyfry. Do napisu wyniku potrzebujesz odpowiadającego jej znaku z alfabetu.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 6</summary>

```python
liczba = int(input())
alfabet = "0123456789ABCDEF"
if liczba < 0:
    print("Błąd danych")
else:
    wynik = ""
    pozostalaLiczba = liczba
    if pozostalaLiczba == 0:
        wynik = "0"
    while pozostalaLiczba > 0:
        reszta = pozostalaLiczba % 16
        wynik = alfabet[reszta] + wynik
        pozostalaLiczba = pozostalaLiczba // 16
    print(wynik)
```

Dla danych `255` wynik:

```text
FF
```

</details>

### Ćwiczenie 7. Odczyt z literami

Wczytaj podstawę od `2` do `16` i niepusty napis. Akceptuj cyfry `0-9` oraz duże litery `A-F`, tylko gdy ich wartości są mniejsze od podstawy. Wypisz wartość dziesiętną albo `Błąd danych`. Sprawdź `16` i `FF`, a także `10` i `A`.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 7</summary>

Obecność znaku w alfabecie nie wystarcza. Sprawdź też jego wartość. Po udanej kontroli użyj tego samego mnożenia przez podstawę co wcześniej.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 7</summary>

```python
podstawa = int(input())
zapisLiczby = input()
alfabet = "0123456789ABCDEF"
czyPoprawny = podstawa >= 2 and podstawa <= 16 and len(zapisLiczby) > 0
for znak in zapisLiczby:
    if znak not in alfabet:
        czyPoprawny = False
    else:
        cyfra = alfabet.index(znak)
        if cyfra >= podstawa:
            czyPoprawny = False
if czyPoprawny:
    wynik = 0
    for znak in zapisLiczby:
        cyfra = alfabet.index(znak)
        wynik = wynik * podstawa + cyfra
    print(wynik)
else:
    print("Błąd danych")
```

Dla danych `16` i `FF` wynik:

```text
255
```

Dla danych `10` i `A` program wypisuje `Błąd danych`.

</details>

## Podsumowanie

Dwa znane algorytmy działają po zastąpieniu stałej podstawy zmienną. Zakres podstaw i zestaw dozwolonych cyfr muszą być zgodne. Konwersja między systemami może składać się z odczytu wartości dziesiętnej i zbudowania nowego zapisu.
