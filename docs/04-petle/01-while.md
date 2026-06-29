# Pętla while w Pythonie - powtarzanie dopóki warunek jest spełniony

## Cel lekcji

Poznasz pętlę `while` i nauczysz się powtarzać instrukcje tak długo, jak warunek jest spełniony.

## Czego się nauczysz

Po tej lekcji będziesz umieć zapisać prostą pętlę `while`, używać licznika, zmieniać wartość zmiennej w pętli oraz rozpoznawać sytuacje, w których pętla może działać bez końca.

## Czym jest pętla while

Pętla `while` to sposób na powtarzanie kodu.

Słowo `while` oznacza dopóki.

Można to rozumieć tak: dopóki warunek jest prawdziwy, wykonuj instrukcje.

Gdy warunek przestaje być prawdziwy, pętla się kończy.

## Koszyk ze smartfonami - jak rozumieć while?

Wyobraź sobie koszyk pełen smartfonów. W koszyku jest 5 smartfonów. Rozdajesz po jednym smartfonie.

Dopóki liczba smartfonów w koszyku jest większa od zera, możesz rozdawać dalej.

Gdy liczba smartfonów spadnie do zera, pętla się kończy.

```python
smartfony = 5

while smartfony > 0:
    print("Rozdaję smartfon. Zostało w koszyku:", smartfony)
    smartfony = smartfony - 1

print("Koszyk jest pusty.")
```

Krok po kroku:

Na początku w koszyku jest `5` smartfonów.

Warunek `smartfony > 0` jest prawdziwy.

Program wypisuje komunikat.

Potem zmniejsza liczbę smartfonów o `1`.

Pętla wraca do sprawdzenia warunku.

Gdy `smartfony` ma wartość `0`, warunek jest fałszywy.

Pętla się kończy.

Program wypisuje komunikat, że koszyk jest pusty.

| smartfony przed obiegiem | warunek smartfony > 0 | smartfony po rozdaniu |
|--------------------------|------------------------|-----------------------|
| 5 | prawda | 4 |
| 4 | prawda | 3 |
| 3 | prawda | 2 |
| 2 | prawda | 1 |
| 1 | prawda | 0 |
| 0 | fałsz | pętla się kończy |

## Składnia pętli while

Podstawowy zapis wygląda tak:

```python
while warunek:
    instrukcje
```

Po `while` wpisujemy warunek.

Po warunku stawiamy dwukropek `:`.

Instrukcje należące do pętli muszą być wcięte.

Po każdym wykonaniu instrukcji program wraca do sprawdzenia warunku.

Jeśli warunek nadal jest prawdziwy, pętla wykonuje się ponownie.

Jeśli warunek jest fałszywy, pętla się kończy.

## Prosty licznik od 1 do 5

```python
licznik = 1

while licznik <= 5:
    print(licznik)
    licznik = licznik + 1

print("Koniec.")
```

Omówienie wiersz po wierszu:

Zmienna `licznik` zaczyna od `1`.

Pętla działa dopóki `licznik` jest mniejszy lub równy `5`.

Program wypisuje aktualną wartość licznika.

Potem zwiększa licznik o `1`.

Gdy licznik osiągnie `6`, warunek `licznik <= 5` jest fałszywy.

Pętla się kończy.

## Jak czytać pętlę while?

Spójrz na fragment:

```python
while licznik <= 5:
    print(licznik)
```

Można to przeczytać tak:

Dopóki `licznik` jest mniejszy lub równy `5`, wypisuj wartość zmiennej `licznik`.

W pętli `while` bardzo ważna jest zmiana wartości zmiennej, która występuje w warunku. Bez tej zmiany pętla może działać bez końca.

## Sumowanie liczb od 1 do n

```python
n = int(input("Podaj n: "))
i = 1
suma = 0

while i <= n:
    suma = suma + i
    i = i + 1

print("Suma wynosi:", suma)
```

Omówienie:

`n` to liczba podana przez użytkownika.

`i` to licznik.

`suma` zaczyna od `0`.

Pętla działa dopóki `i <= n`.

W każdym obiegu dodajemy `i` do sumy.

Potem zwiększamy `i` o `1`.

Po zakończeniu pętli wypisujemy sumę.

## Pytanie o hasło bez break

```python
haslo = ""

while haslo != "python":
    haslo = input("Podaj hasło: ")

print("Hasło poprawne.")
```

Omówienie:

Na początku zmienna `haslo` jest pusta.

Pętla działa dopóki hasło jest różne od `"python"`.

Użytkownik wpisuje hasło.

Gdy wpisze `"python"`, warunek staje się fałszywy.

Pętla się kończy.

Program wypisuje komunikat.

## Różnica między if i while

`if` sprawdza warunek i może wykonać kod jeden raz.

`while` sprawdza warunek i może wykonywać kod wiele razy, dopóki warunek jest prawdziwy.

## Typowe błędy uczniów

### Brak dwukropka po warunku while

```python
licznik = 1

while licznik <= 5
    print(licznik)
    licznik = licznik + 1
```

Po warunku `while` musi być dwukropek `:`.

### Brak wcięcia instrukcji należących do pętli

```python
licznik = 1

while licznik <= 5:
print(licznik)
licznik = licznik + 1
```

Instrukcje należące do pętli muszą być wcięte.

### Zapomnienie o zmianie zmiennej użytej w warunku

```python
licznik = 1

while licznik <= 5:
    print(licznik)
```

Ten program może działać bez końca, bo wartość zmiennej `licznik` nigdy się nie zmienia.

### Stworzenie pętli nieskończonej

Pętla nieskończona powstaje wtedy, gdy warunek cały czas jest prawdziwy.

Zawsze sprawdzaj, czy w pętli zmienia się coś, co może zakończyć pętlę.

### Mylenie while z if

`if` sprawdza warunek raz.

`while` wraca do warunku wiele razy.

### Myślenie, że while wykona się tylko raz

Pętla `while` może wykonać się wiele razy. Zależy to od warunku.

### Zwiększanie licznika w złym miejscu

Licznik powinien zmieniać się wewnątrz pętli. Jeśli zmienisz go w złym miejscu, pętla może działać za długo, za krótko albo bez końca.

### Wypisywanie wyniku końcowego wewnątrz pętli

```python
n = int(input("Podaj n: "))
i = 1
suma = 0

while i <= n:
    suma = suma + i
    i = i + 1
    print("Suma wynosi:", suma)
```

Ten kod wypisuje wynik po każdym obiegu pętli. Jeśli chcemy wypisać tylko wynik końcowy, `print()` powinien być po pętli, bez wcięcia.

### Mylenie = oraz ==

Znak `=` służy do przypisania wartości do zmiennej.

Znak `==` służy do porównywania wartości.

### Zapomnienie o początkowej wartości zmiennej przed pętlą

Przed pętlą trzeba przygotować zmienną, która występuje w warunku.

```python
licznik = 1

while licznik <= 5:
    print(licznik)
    licznik = licznik + 1
```

Tutaj zmienna `licznik` ma wartość początkową przed pętlą.

## Ćwiczenia

1. Wypisz liczby od 1 do 5 za pomocą pętli while.
2. Wypisz liczby od 1 do 10 za pomocą pętli while.
3. Wypisz liczby od 10 do 1 za pomocą pętli while.
4. Wczytaj liczbę n i wypisz liczby od 1 do n.
5. Wczytaj liczbę n i oblicz sumę liczb od 1 do n.
6. Wczytaj liczbę n i oblicz iloczyn liczb od 1 do n.
7. Wczytaj liczbę smartfonów w koszyku i wypisuj komunikat o rozdawaniu smartfonów, aż koszyk będzie pusty.
8. Napisz program, który pyta użytkownika o hasło tak długo, aż wpisze "python".
9. Wczytaj liczbę n i wypisz kolejne liczby parzyste od 2 do n.
10. Napisz program, który odlicza od podanej liczby do zera.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
