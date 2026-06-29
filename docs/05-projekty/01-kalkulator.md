# Mini kalkulator kosztów zakupów

## Cel projektu

Celem projektu jest napisanie programu, który oblicza koszt zakupów na podstawie danych wpisanych przez użytkownika.

Projekt łączy podstawowe elementy Pythona: `print()`, zmienne, typy danych, `input()`, konwersję typów, operatory oraz instrukcje warunkowe `if`, `if-else` i `elif`.

## Co program ma robić

Program ma:

- zapytać o nazwę produktu,
- zapytać o cenę netto jednej sztuki,
- zapytać o liczbę sztuk,
- zapytać o stawkę VAT w procentach,
- obliczyć wartość netto,
- obliczyć kwotę VAT,
- obliczyć wartość brutto,
- wypisać czytelne podsumowanie zakupów.

## Wymagania funkcjonalne

Program powinien wczytać dane od użytkownika i wykonać obliczenia.

Wersja podstawowa oblicza wartość netto, kwotę VAT i wartość brutto.

Wersja z warunkiem dodatkowo wypisuje, czy są to małe czy większe zakupy.

Wersja rozszerzona klasyfikuje zakupy jako małe, średnie albo duże.

## Wymagania techniczne

W projekcie używamy:

- zmiennych,
- `print()`,
- `input()`,
- `int()`,
- `float()`,
- operatorów arytmetycznych,
- instrukcji `if`, `elif`, `else`.

W projekcie nie używamy:

- list,
- funkcji własnych,
- pętli,
- klas,
- plików,
- bibliotek zewnętrznych.

## Przykładowe działanie programu

```text
Podaj nazwę produktu: pendrive
Podaj cenę netto jednej sztuki: 20
Podaj liczbę sztuk: 3
Podaj stawkę VAT w procentach: 23

Podsumowanie zakupów
Produkt: pendrive
Cena netto jednej sztuki: 20.0 zł
Liczba sztuk: 3
Wartość netto: 60.0 zł
Kwota VAT: 13.8 zł
Wartość brutto: 73.8 zł
```

## Wersja podstawowa

Program pyta użytkownika o nazwę produktu, cenę netto jednej sztuki, liczbę sztuk oraz stawkę VAT.

Następnie wykonuje obliczenia:

```python
wartosc_netto = cena_netto * liczba_sztuk
kwota_vat = wartosc_netto * stawka_vat / 100
wartosc_brutto = wartosc_netto + kwota_vat
```

Program wypisuje podsumowanie:

```text
Produkt: ...
Cena netto jednej sztuki: ...
Liczba sztuk: ...
Wartość netto: ...
Kwota VAT: ...
Wartość brutto: ...
```

## Przykładowy kod wersji podstawowej

```python
print("Mini kalkulator kosztów zakupów")

produkt = input("Podaj nazwę produktu: ")
cena_netto = float(input("Podaj cenę netto jednej sztuki: "))
liczba_sztuk = int(input("Podaj liczbę sztuk: "))
stawka_vat = float(input("Podaj stawkę VAT w procentach: "))

wartosc_netto = cena_netto * liczba_sztuk
kwota_vat = wartosc_netto * stawka_vat / 100
wartosc_brutto = wartosc_netto + kwota_vat

print()
print("Podsumowanie zakupów")
print("Produkt:", produkt)
print("Cena netto jednej sztuki:", cena_netto, "zł")
print("Liczba sztuk:", liczba_sztuk)
print("Wartość netto:", wartosc_netto, "zł")
print("Kwota VAT:", kwota_vat, "zł")
print("Wartość brutto:", wartosc_brutto, "zł")
```

## Wersja z prostym if

Dodaj do programu prostą ocenę wartości zakupów.

Jeżeli wartość brutto jest większa niż `100`, program wypisuje:

```text
To są większe zakupy.
```

W przeciwnym razie program wypisuje:

```text
To są małe zakupy.
```

Przykład:

```python
if wartosc_brutto > 100:
    print("To są większe zakupy.")
else:
    print("To są małe zakupy.")
```

## Wersja rozszerzona

W wersji rozszerzonej użyj `if`, `elif` i `else`.

Jeżeli wartość brutto:

- jest mniejsza niż `50`, wypisz: `Małe zakupy.`,
- jest od `50` do `200`, wypisz: `Średnie zakupy.`,
- jest większa lub równa `200`, wypisz: `Duże zakupy.`

Przykład:

```python
if wartosc_brutto < 50:
    print("Małe zakupy.")
elif wartosc_brutto < 200:
    print("Średnie zakupy.")
else:
    print("Duże zakupy.")
```

## Etapy wykonania projektu

1. Utwórz plik projektu.
2. Wypisz tytuł programu.
3. Wczytaj nazwę produktu.
4. Wczytaj cenę netto jednej sztuki.
5. Wczytaj liczbę sztuk.
6. Wczytaj stawkę VAT.
7. Oblicz wartość netto.
8. Oblicz kwotę VAT.
9. Oblicz wartość brutto.
10. Wypisz podsumowanie.
11. Dodaj prostą ocenę wielkości zakupów za pomocą `if` / `elif` / `else`.
12. Przetestuj program dla kilku danych.

## Podpowiedzi

Nazwa produktu jest tekstem, więc użyj `input()`.

Cena netto może być liczbą rzeczywistą, więc użyj `float()`.

Liczba sztuk jest liczbą całkowitą, więc użyj `int()`.

Stawka VAT może być liczbą rzeczywistą, więc użyj `float()`.

Do wypisywania wyników możesz używać `print()` z przecinkami.

Dla chętnych można użyć f-stringów i zaokrąglenia do dwóch miejsc po kropce.

Przykład:

```python
print(f"Wartość brutto: {wartosc_brutto:.2f} zł")
```

Zapis `:.2f` oznacza dwa miejsca po kropce.

## Co uczeń ma dodać od siebie?

Do projektu dodaj minimum 5 samodzielnych zmian.

Co najmniej jedna zmiana musi wpływać na działanie programu, a nie tylko na tekst komunikatów.

Nie musisz wymyślać wszystkich zmian samodzielnie. Możesz wybrać propozycje z listy, ale program ma być spójny i działać poprawnie.

## Przykłady zmian, które możesz dodać

1. Koszt dostawy

Program pyta użytkownika o koszt dostawy i dodaje go do ceny końcowej.

Przykład zmiennych:

```python
koszt_dostawy
wartosc_z_dostawa
```

2. Rabat po przekroczeniu kwoty

Jeżeli wartość brutto jest większa niż `100` zł, program nalicza rabat `10%`.

Przykład komunikatu:

```text
Przyznano rabat 10%.
```

3. Wybór typu klienta

Program pyta, czy klient jest uczniem, nauczycielem czy innym klientem.

Dla ucznia może być rabat `5%`, dla nauczyciela `10%`, a dla pozostałych brak rabatu.

4. Opakowanie prezentowe

Program pyta, czy doliczyć koszt opakowania prezentowego.

Na tym etapie można zrobić prostą wersję: użytkownik wpisuje koszt opakowania, a program dodaje go do końcowej ceny.

5. Klasyfikacja zakupów

Program wypisuje:

- `Małe zakupy`, gdy wartość brutto jest mniejsza niż `50` zł,
- `Średnie zakupy`, gdy wartość brutto jest od `50` do `200` zł,
- `Duże zakupy`, gdy wartość brutto jest większa lub równa `200` zł.

6. Inna stawka VAT

Program pozwala wybrać albo wpisać inną stawkę VAT, na przykład `5%`, `8%` albo `23%`.

7. Cena za kilka produktów tego samego typu

Program pyta o cenę jednego produktu i liczbę sztuk, a potem oblicza koszt całkowity.

8. Podsumowanie paragonu

Program wypisuje wynik w formie prostego paragonu, na przykład:

```text
--- PARAGON ---
Produkt: pendrive
Liczba sztuk: 3
Cena netto: 60.00 zł
VAT: 13.80 zł
Razem brutto: 73.80 zł
```

9. Zaokrąglenie wyniku

Program wypisuje kwoty do dwóch miejsc po kropce za pomocą f-stringów.

Przykład:

```python
print(f"Wartość brutto: {wartosc_brutto:.2f} zł")
```

10. Komentarze w kodzie

Uczeń dodaje krótkie komentarze wyjaśniające najważniejsze obliczenia, na przykład:

```python
# Obliczamy wartość netto całych zakupów
wartosc_netto = cena_netto * liczba_sztuk
```

## Przykładowy zestaw zmian dla ucznia

Uczeń może wybrać na przykład taki zestaw 5 zmian:

1. Zmienić tytuł programu.
2. Dodać koszt dostawy.
3. Dodać rabat 10% po przekroczeniu 100 zł.
4. Wypisać paragon z pustymi liniami.
5. Sformatować kwoty do dwóch miejsc po kropce.

Drugi przykładowy zestaw:

1. Zmienić komunikaty dla użytkownika.
2. Dodać wybór stawki VAT.
3. Dodać klasyfikację zakupów: małe, średnie, duże.
4. Dodać komentarz przy obliczaniu VAT.
5. Dodać komunikat końcowy z podziękowaniem.

## Kryteria zaliczenia

Program jest zaliczony, jeżeli:

- uruchamia się bez błędów,
- wczytuje dane od użytkownika,
- poprawnie zamienia tekst na liczby,
- poprawnie oblicza wartość netto,
- poprawnie oblicza kwotę VAT,
- poprawnie oblicza wartość brutto,
- wypisuje czytelne podsumowanie,
- używa poprawnych nazw zmiennych,
- zawiera przynajmniej jeden sensowny komentarz,
- zawiera prostą instrukcję `if` / `elif` / `else` w wersji rozszerzonej.

## Czego nie robić

Nie wpisuj wszystkich danych na stałe. Program ma pytać użytkownika.

Nie używaj zmiennych o nazwach `x`, `y`, `z`, jeśli można użyć czytelnych nazw.

Nie mieszaj ceny netto i brutto.

Nie zapominaj o konwersji `float()` i `int()`.

Nie wypisuj samej liczby bez opisu.

Nie kopiuj programu bez zrozumienia.

## Sposób oddania pracy

Uczeń zapisuje projekt w swoim folderze w JupyterLab.

Nazwa pliku:

```text
projekt_01_kalkulator_zakupow.py
```

Uczeń może najpierw testować rozwiązanie w notebooku, ale ostateczna wersja powinna być zapisana jako plik `.py`.
