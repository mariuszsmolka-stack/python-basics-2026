# Komentarze w Pythonie - po co są i jak pisać je poprawnie

## Cel lekcji

Poznasz komentarze w Pythonie i nauczysz się pisać takie komentarze, które pomagają zrozumieć program.

## Czego się nauczysz

Po tej lekcji będziesz umieć dodać komentarz w osobnej linii, komentarz na końcu linii kodu oraz tymczasowo wyłączyć linię programu. Nauczysz się też odróżniać dobry komentarz od zbędnego.

## Czym jest komentarz

Komentarz to tekst w programie, który jest przeznaczony dla człowieka, a nie dla Pythona. Python pomija komentarze podczas wykonywania programu.

Komentarz pomaga osobie czytającej kod zrozumieć, po co powstał dany fragment programu.

## Znak #

W Pythonie komentarz zaczyna się od znaku `#`.

```python
# To jest komentarz
print("Cześć!")
```

Omówienie:

Wiersz zaczynający się od `#` jest komentarzem.

Python go nie wykonuje.

Program wykona tylko instrukcję `print("Cześć!")`.

## Komentarz w osobnej linii

Komentarz może znajdować się w osobnej linii.

```python
# Obliczamy pole prostokąta
dlugosc = 8
szerokosc = 4
pole = dlugosc * szerokosc

print("Pole prostokąta wynosi:", pole)
```

Komentarz informuje, jaki jest cel fragmentu programu.

## Komentarz na końcu linii kodu

Komentarz może też znajdować się na końcu linii kodu.

```python
wiek = 16  # wiek ucznia w latach
```

Komentarz zaczyna się od znaku `#`.

Wszystko po znaku `#` w tej linii jest komentarzem.

Kod przed znakiem `#` nadal się wykonuje.

## Komentarz jako opis fragmentu programu

Komentarz może krótko opisać, co oznacza dany fragment programu.

```python
# Obliczamy łączny koszt zakupu
cena = 12
liczba_sztuk = 3
koszt = cena * liczba_sztuk

print("Koszt wynosi:", koszt)
```

Taki komentarz pomaga zrozumieć cel obliczenia.

## Komentarz jako tymczasowe wyłączenie kodu

Komentarz może tymczasowo wyłączyć linię kodu.

```python
print("Początek programu")
# print("Ten wiersz jest chwilowo wyłączony")
print("Koniec programu")
```

Druga instrukcja `print()` nie wykona się.

Została zamieniona w komentarz.

Taki sposób bywa używany podczas testowania programu.

## Kiedy komentarz jest dobry

Komentarz jest dobry, gdy pomaga zrozumieć program.

Dobry komentarz wyjaśnia cel fragmentu kodu, znaczenie zmiennej albo powód użycia danego rozwiązania.

Komentarz powinien być krótki i konkretny.

## Kiedy komentarz jest zły lub zbędny

Komentarz jest zły, gdy niczego nie wyjaśnia.

Komentarz jest zbędny, gdy tylko powtarza to, co dokładnie widać w kodzie.

Zbyt wiele komentarzy może utrudnić czytanie programu.

## Komentarz ma wyjaśniać zamiar, a nie przepisywać kod

Dobry komentarz odpowiada na pytanie:

Po co robimy dany krok?

Co oznacza dana część programu?

Dlaczego zastosowano takie rozwiązanie?

Zły komentarz tylko powtarza to, co już dokładnie widać w kodzie.

Zły lub zwykle zbędny komentarz:

```python
x = x + 1  # zwiększamy x o 1
```

Ten komentarz jest zwykle zbędny, bo kod jest prosty i mówi to samo.

Lepszy komentarz:

```python
liczba_prob += 1  # zapamiętujemy kolejną próbę wpisania hasła
```

Ten komentarz mówi, co oznacza zwiększenie licznika w kontekście programu.

## Dobre i złe komentarze

| Kod z komentarzem | Ocena | Dlaczego? |
|-------------------|-------|-----------|
| # Obliczamy koszt całego zamówienia | dobry | wyjaśnia cel fragmentu programu |
| # Sprawdzamy, czy użytkownik podał poprawne hasło | dobry | wyjaśnia sens warunku |
| suma = suma + liczba  # dodajemy liczbę do sumy | czasem zbędny | kod jest prosty i komentarz tylko go powtarza |
| x = 5  # x równa się 5 | zły | komentarz niczego nie wyjaśnia |
| # tutaj coś liczymy | zły | komentarz jest zbyt ogólny |

## Kiedy warto pisać komentarze?

Warto pisać komentarze, gdy fragment programu ma konkretny cel.

Warto pisać komentarze, gdy obliczenie może nie być od razu oczywiste.

Warto pisać komentarze, gdy chcemy oddzielić części programu.

Warto pisać komentarze, gdy chcemy wyjaśnić znaczenie zmiennej lub wzoru.

Warto pisać komentarze, gdy tymczasowo wyłączamy fragment kodu podczas testowania.

## Kiedy komentarz jest zbędny?

Komentarz jest zbędny, gdy kod jest bardzo prosty.

Komentarz jest zbędny, gdy tylko powtarza kod.

Komentarz jest zbędny, gdy nazwy zmiennych są już czytelne.

Komentarz jest zbędny, gdy nie dodaje żadnej informacji.

Przykład zbędnego komentarza:

```python
wiek = 16  # przypisujemy 16 do zmiennej wiek
```

Lepsza wersja bez komentarza:

```python
wiek = 16
```

Czasem lepsza jest dobra nazwa zmiennej niż komentarz.

Zła wersja:

```python
x = 23  # podatek VAT w procentach
```

Lepsza wersja:

```python
stawka_vat = 23
```

Dobra nazwa zmiennej często zmniejsza potrzebę pisania komentarza.

## Komentarze a czytelny kod

Komentarz pomaga, ale nie naprawia źle napisanego programu.

Najpierw staramy się pisać czytelny kod: dobre nazwy zmiennych, proste instrukcje, jasny układ.

Dopiero potem dodajemy komentarze tam, gdzie naprawdę pomagają.

Komentarz nie zastępuje czytelnego kodu.

## Typowe błędy uczniów

### Pisanie komentarza bez znaku #

```python
To jest komentarz
print("Cześć")
```

Python potraktuje pierwszy wiersz jak kod i zgłosi błąd.

### Umieszczanie znaku # w złym miejscu

```python
pole = dlugosc # * szerokosc
```

Wszystko po `#` jest komentarzem, więc mnożenie nie zostanie wykonane.

### Myślenie, że komentarz zostanie wypisany na ekranie

Komentarz nie pojawi się na ekranie. Na ekranie pojawia się tekst z `print()`.

### Komentowanie każdej linii programu

Nie trzeba komentować każdej linii. Komentarze mają pomagać, a nie zasłaniać kod.

### Komentarze, które tylko powtarzają kod

```python
suma = suma + liczba  # dodajemy liczbę do sumy
```

Taki komentarz często jest zbędny.

### Komentarze zbyt ogólne

```python
# tutaj coś liczymy
```

Ten komentarz jest zbyt ogólny. Nie mówi, co i po co liczymy.

### Nieaktualne komentarze

Jeśli zmienisz kod, sprawdź też komentarze. Nieaktualny komentarz może wprowadzać w błąd.

### Mylenie komentarza z tekstem w print()

```python
# To jest komentarz
print("To zostanie wypisane na ekranie")
```

Komentarz nie pojawi się na ekranie.

Tekst w `print()` pojawi się na ekranie.

### Używanie komentarza zamiast dobrej nazwy zmiennej

Zamiast pisać `x = 23  # podatek VAT`, lepiej użyć nazwy `stawka_vat`.

### Zostawianie wyłączonego kodu bez informacji

Jeśli wyłączasz linię kodu komentarzem na dłużej, warto wiedzieć, dlaczego została wyłączona.

## Krótka zasada

Dobry komentarz nie mówi tylko, co robi kod. Dobry komentarz wyjaśnia, po co ten kod jest w programie.

## Ćwiczenia

1. Dopisz komentarz na początku programu, który wypisuje Twoje imię i wiek.
2. Napisz program obliczający pole prostokąta i dodaj komentarz wyjaśniający cel obliczenia.
3. Napisz program obliczający cenę brutto i dodaj komentarz wyjaśniający, czym jest stawka VAT.
4. Popraw zły komentarz: x = x + 1  # dodajemy 1 do x
5. Popraw zły komentarz: # tutaj coś liczymy
6. Usuń zbędny komentarz z kodu: wiek = 16  # przypisujemy 16 do zmiennej wiek
7. Zamień złą nazwę zmiennej i komentarz na lepszą nazwę zmiennej: x = 23  # podatek VAT w procentach
8. Napisz trzy linie kodu z print() i jedną z nich tymczasowo wyłącz komentarzem.
9. Napisz krótki program z dwoma komentarzami: jeden dobry komentarz i jeden komentarz, który potem usuniesz jako zbędny.
10. Wyjaśnij własnymi słowami, czym różni się komentarz od tekstu wypisywanego przez print().

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
