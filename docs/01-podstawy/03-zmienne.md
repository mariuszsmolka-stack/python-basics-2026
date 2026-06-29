# Zmienne w Pythonie - nazwy, wartości i proste obliczenia

## Cel lekcji

Poznasz zmienne w Pythonie i nauczysz się używać ich do zapamiętywania wartości oraz wykonywania prostych obliczeń.

## Czego się nauczysz

Po tej lekcji będziesz umieć tworzyć zmienne, nadawać im nazwy, przypisywać wartości, zmieniać wartości i używać zmiennych w `print()`.

## Czym jest zmienna

Zmienna to nazwa, pod którą program zapamiętuje jakąś wartość.

Zmienną można porównać do podpisanej szufladki. Na szufladce jest nazwa, na przykład `wiek`. W środku znajduje się wartość, na przykład `16`.

Gdy w programie piszemy `wiek`, Python sięga do tej szufladki i bierze zapisaną wartość.

## Po co używamy zmiennych

Zmiennych używamy po to, aby program mógł coś zapamiętać.

Może to być liczba, tekst, wynik obliczenia albo inna wartość.

Dzięki zmiennym nie musimy wpisywać tej samej wartości wiele razy. Możemy też łatwo zmienić dane w jednym miejscu.

## Nazwa i wartość zmiennej

Zmienna ma nazwę i wartość.

Nazwa zmiennej pozwala później odwołać się do zapisanej wartości.

Przykład:

```python
wiek = 16
```

`wiek` to nazwa zmiennej.

`16` to wartość zmiennej.

Znak `=` oznacza: zapisz wartość `16` pod nazwą `wiek`.

## Co oznacza znak =

W Pythonie znak `=` oznacza przypisanie wartości.

Nie jest to pytanie o równość.

To polecenie dla komputera: zapamiętaj wartość po prawej stronie pod nazwą po lewej stronie.

## Jak czytać przypisanie?

Przykład:

```python
liczba = 10
```

Czytamy to tak:

Do zmiennej `liczba` przypisz wartość `10`.

Albo:

Pod nazwą `liczba` zapamiętaj wartość `10`.

Tego nie czytamy jako pytania: czy liczba równa się 10? To jest polecenie przypisania wartości.

## Zapisanie liczby w zmiennej

```python
punkty = 25
print(punkty)
```

W pierwszym wierszu zapisujemy liczbę `25` w zmiennej `punkty`.

W drugim wierszu wypisujemy wartość zmiennej `punkty`.

## Zapisanie tekstu w zmiennej

```python
imie = "Anna"
print(imie)
```

W pierwszym wierszu zapisujemy tekst `"Anna"` w zmiennej `imie`.

W drugim wierszu wypisujemy wartość zmiennej `imie`.

Python wypisze `Anna`.

## Użycie zmiennej w print()

```python
miasto = "Kraków"
print("Mieszkam w mieście:", miasto)
```

Funkcja `print()` może wypisywać tekst oraz wartość zmiennej. W tym przykładzie wypisze komunikat i wartość zmiennej `miasto`.

## Zmiana wartości zmiennej

```python
punkty = 10
print(punkty)

punkty = 15
print(punkty)
```

Omówienie:

Najpierw zmienna `punkty` ma wartość `10`.

Potem do tej samej zmiennej przypisujemy nową wartość `15`.

Stara wartość zostaje zastąpiona.

Zmienna w danym momencie przechowuje jedną aktualną wartość.

## Proste obliczenie z użyciem zmiennych

```python
a = 5
b = 3
suma = a + b
print(suma)
```

Omówienie:

`a` przechowuje `5`.

`b` przechowuje `3`.

`suma` przechowuje wynik dodawania `a + b`.

`print(suma)` wypisuje wynik.

## Pole prostokąta

```python
dlugosc = 8
szerokosc = 4
pole = dlugosc * szerokosc
print("Pole prostokąta wynosi:", pole)
```

Omówienie wiersz po wierszu:

Pierwszy wiersz zapisuje długość prostokąta w zmiennej `dlugosc`.

Drugi wiersz zapisuje szerokość prostokąta w zmiennej `szerokosc`.

Trzeci wiersz mnoży długość przez szerokość i zapisuje wynik w zmiennej `pole`.

Czwarty wiersz wypisuje komunikat oraz wynik obliczenia.

## Jak nazywać zmienne?

Nazwa zmiennej powinna mówić, co przechowuje.

Nazwa może zawierać litery, cyfry i znak podkreślenia.

Nazwa nie może zaczynać się od cyfry.

W nazwach zmiennych nie używamy spacji.

W Pythonie wielkość liter ma znaczenie.

Lepiej używać prostych nazw bez polskich znaków.

Dla początkujących najlepsze są nazwy małymi literami, na przykład `imie`, `wiek`, `suma`, `pole_prostokata`.

## Dobre i złe nazwy zmiennych

Dobre nazwy:

| Dobra nazwa | Dlaczego dobra? |
|-------------|-----------------|
| wiek | wiadomo, że przechowuje wiek |
| imie | wiadomo, że przechowuje imię |
| liczba_punktow | wiadomo, że przechowuje punkty |
| pole_prostokata | wiadomo, że przechowuje pole prostokąta |
| cena_netto | wiadomo, że przechowuje cenę netto |

Złe nazwy:

| Zła nazwa | Dlaczego zła? |
|-----------|---------------|
| x | czasem może być dobra, ale często nic nie wyjaśnia |
| a1 | mało czytelna |
| mojazmienna | za mało konkretna |
| liczba punktow | zawiera spację |
| 2liczba | zaczyna się od cyfry |
| imię | zawiera polski znak, lepiej użyć imie |

Python pozwala używać wielu różnych nazw, ale w nauce programowania najważniejsza jest czytelność.

## Wielkość liter ma znaczenie

```python
wiek = 16
Wiek = 18

print(wiek)
print(Wiek)
```

Dla Pythona `wiek` i `Wiek` to dwie różne zmienne.

Pierwsza ma wartość `16`, a druga ma wartość `18`.

## Typowe błędy uczniów

### Mylenie znaku = z porównaniem

W Pythonie `=` przypisuje wartość do zmiennej. Nie pyta, czy dwie rzeczy są równe.

### Użycie zmiennej przed przypisaniem jej wartości

```python
wiek = 16
print(wiek_ucznia)
```

Program zgłosi błąd, bo zmienna `wiek_ucznia` nie została wcześniej utworzona.

### Literówka w nazwie zmiennej

```python
liczba = 10
print(lizcba)
```

Dla Pythona `liczba` i `lizcba` to dwie różne nazwy.

### Użycie spacji w nazwie zmiennej

```python
liczba punktow = 20
```

W nazwie zmiennej nie używamy spacji. Lepiej napisać:

```python
liczba_punktow = 20
```

### Rozpoczęcie nazwy zmiennej od cyfry

```python
2liczba = 10
```

Nazwa zmiennej nie może zaczynać się od cyfry.

### Mylenie wielkich i małych liter

`wiek` i `Wiek` to dwie różne zmienne.

### Nazwy, które nic nie mówią

Nazwa `x` czasem bywa używana, ale dla początkujących lepiej pisać pełniejsze nazwy, na przykład `wiek` albo `suma`.

### Myślenie, że zmienna może mieć kilka wartości naraz

Zmienna przechowuje jedną aktualną wartość.

### Zapominanie, że nowa wartość zastępuje starą

Jeśli przypiszesz nową wartość do tej samej zmiennej, stara wartość zostaje zastąpiona.

### Próba wypisania tekstu bez cudzysłowu

```python
print(Anna)
```

Python potraktuje `Anna` jak nazwę zmiennej. Jeśli chcemy wypisać tekst, używamy cudzysłowu:

```python
print("Anna")
```

## Ćwiczenia

1. Utwórz zmienną imie i przypisz do niej swoje imię. Wypisz ją na ekranie.
2. Utwórz zmienną wiek i przypisz do niej swój wiek. Wypisz ją na ekranie.
3. Utwórz zmienne a i b z dowolnymi liczbami. Oblicz ich sumę.
4. Utwórz zmienne dlugosc i szerokosc. Oblicz pole prostokąta.
5. Utwórz zmienne cena i liczba_sztuk. Oblicz łączny koszt.
6. Utwórz zmienną punkty z wartością 10. Wypisz ją, potem zmień jej wartość na 20 i wypisz ponownie.
7. Utwórz zmienne imie i nazwisko. Wypisz zdanie z imieniem i nazwiskiem.
8. Utwórz zmienną temperatura i wypisz komunikat z jej wartością.
9. Utwórz zmienne rok_obecny i rok_urodzenia. Oblicz przybliżony wiek.
10. Popraw błędne nazwy zmiennych: 2liczba, liczba punktow, imię ucznia, cena-netto.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
