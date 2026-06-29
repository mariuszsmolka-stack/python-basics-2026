# break i continue w pętlach — przerywanie i pomijanie obiegu

## Cel lekcji

Celem lekcji jest zrozumienie, jak przerwać działanie pętli za pomocą `break` oraz jak pominąć jeden obieg pętli za pomocą `continue`.

## Czego się nauczysz

Po tej lekcji będziesz umieć:

1. wyjaśnić, czym jest `break`,
2. wyjaśnić, czym jest `continue`,
3. odróżnić przerwanie całej pętli od pominięcia jednego obiegu,
4. używać `break` w pętli `while` i `for`,
5. używać `continue` w pętli `while` i `for`,
6. unikać prostych błędów prowadzących do pętli nieskończonej.

## Krótkie przypomnienie, czym jest pętla

Pętla pozwala powtarzać instrukcje wiele razy.

Pętla `while` działa dopóki warunek jest prawdziwy.

Pętla `for` przechodzi przez kolejne wartości, na przykład z `range()`.

Czasami chcemy przerwać pętlę wcześniej. Czasami chcemy pominąć tylko jeden obieg pętli. Do tego służą instrukcje `break` i `continue`.

Można to porównać do kolejki zadań.

`break` oznacza: kończymy całą pracę, dalej już nie sprawdzamy.

`continue` oznacza: to jedno zadanie pomijam, ale przechodzę do następnego.

## break — przerwanie całej pętli

Instrukcja `break` oznacza: przerwij całą pętlę natychmiast.

Po wykonaniu `break` program wychodzi z pętli i przechodzi do pierwszej instrukcji zapisanej po pętli.

Przykład:

```python
while True:
    haslo = input("Podaj hasło: ")

    if haslo == "python":
        print("Hasło poprawne.")
        break

    print("Hasło niepoprawne. Spróbuj ponownie.")

print("Koniec programu.")
```

Omówienie:

1. `while True` tworzy pętlę, która mogłaby działać bez końca.
2. Program prosi użytkownika o wpisanie hasła.
3. Instrukcja `if` sprawdza, czy hasło jest równe `"python"`.
4. Jeśli hasło jest poprawne, program wypisuje komunikat.
5. Instrukcja `break` przerywa całą pętlę.
6. Program przechodzi do instrukcji po pętli.
7. Jeśli hasło jest niepoprawne, program wypisuje komunikat i pyta ponownie.

`while True` z instrukcją `break` jest poprawnym sposobem pisania programu, ale trzeba używać go świadomie. Bez `break` taka pętla może działać bez końca.

## break w pętli for

Instrukcji `break` można użyć także w pętli `for`.

Przykład:

```python
szukana = 7

for liczba in range(1, 11):
    print("Sprawdzam:", liczba)

    if liczba == szukana:
        print("Znalazłem liczbę.")
        break

print("Koniec szukania.")
```

Omówienie:

1. Zmienna `szukana` przechowuje liczbę, której szukamy.
2. Pętla sprawdza liczby od 1 do 10.
3. Program wypisuje aktualnie sprawdzaną liczbę.
4. Jeśli `liczba == szukana`, program wypisuje komunikat.
5. Instrukcja `break` kończy pętlę.
6. Liczby po 7 nie będą już sprawdzane.

## continue — pominięcie obecnego obiegu

Instrukcja `continue` oznacza: pomiń resztę obecnego obiegu pętli i przejdź do następnego obiegu.

`continue` nie kończy całej pętli. Pomija tylko ten jeden obieg.

Przykład:

```python
for liczba in range(1, 11):
    if liczba == 5:
        continue

    print(liczba)
```

Omówienie:

1. Pętla przechodzi przez liczby od 1 do 10.
2. Gdy `liczba` ma wartość 5, wykonuje się `continue`.
3. Program pomija wtedy instrukcję `print(liczba)`.
4. Liczba 5 nie zostanie wypisana.
5. Pętla działa dalej dla kolejnych liczb.

Drugi przykład:

```python
for liczba in range(1, 11):
    if liczba % 2 == 0:
        continue

    print("Liczba nieparzysta:", liczba)
```

Omówienie:

1. Operator `%` zwraca resztę z dzielenia.
2. Warunek `liczba % 2 == 0` sprawdza, czy liczba jest parzysta.
3. Jeśli liczba jest parzysta, program pomija dalsze instrukcje w tym obiegu.
4. Wypisane zostaną tylko liczby nieparzyste.

## continue w pętli while

Instrukcji `continue` można użyć także w pętli `while`.

Przykład:

```python
licznik = 0

while licznik < 10:
    licznik += 1

    if licznik == 5:
        continue

    print(licznik)
```

Omówienie:

1. Zmienna `licznik` zaczyna od 0.
2. Pętla działa, dopóki `licznik < 10`.
3. Na początku każdego obiegu licznik zwiększa się o 1.
4. Gdy licznik ma wartość 5, wykonuje się `continue`.
5. Program pomija wtedy `print(licznik)`.
6. Liczba 5 nie zostanie wypisana.
7. Pętla działa dalej.

W pętli `while` trzeba szczególnie uważać. Jeśli `continue` wykona się przed zmianą licznika, program może utworzyć pętlę nieskończoną.

Zły przykład:

```python
licznik = 0

while licznik < 10:
    if licznik == 5:
        continue

    licznik += 1
    print(licznik)
```

Ten program może zatrzymać się na wartości 5. Gdy `licznik == 5`, wykonuje się `continue`, więc program wraca na początek pętli. Licznik nie zwiększa się dalej.

## break a continue — najważniejsza różnica

| Instrukcja | Co robi? | Czy kończy całą pętlę? |
| --- | --- | --- |
| `break` | przerywa pętlę | tak |
| `continue` | pomija obecny obieg | nie |

Najprościej:

`break` mówi: kończę całą pętlę.

`continue` mówi: pomijam ten jeden obieg i lecę dalej.

## Jak czytać kod z break?

Przykład:

```python
if haslo == "python":
    break
```

Czytamy to tak:

Jeżeli hasło jest poprawne, przerwij całą pętlę.

## Jak czytać kod z continue?

Przykład:

```python
if liczba % 2 == 0:
    continue
```

Czytamy to tak:

Jeżeli liczba jest parzysta, pomiń dalsze instrukcje w tym obiegu pętli i przejdź do następnej liczby.

## Kiedy używać break?

Instrukcji `break` warto użyć, gdy:

1. znaleźliśmy szukaną wartość i nie trzeba sprawdzać dalej,
2. użytkownik wpisał poprawne hasło,
3. użytkownik chce zakończyć działanie programu,
4. dalsze powtarzanie pętli nie ma już sensu.

## Kiedy używać continue?

Instrukcji `continue` warto użyć, gdy:

1. chcemy pominąć niektóre wartości,
2. dane w danym obiegu nie spełniają warunku,
3. nie chcemy wykonywać dalszych instrukcji dla konkretnego przypadku,
4. pętla ma działać dalej, ale bez obecnego obiegu.

## Kiedy nie używać break i continue?

Nie każda pętla potrzebuje `break` albo `continue`.

Czasami lepiej zapisać jasny warunek pętli.

Przykład bez `break`:

```python
haslo = ""

while haslo != "python":
    haslo = input("Podaj hasło: ")

print("Hasło poprawne.")
```

Ten zapis jest prosty. Warunek pętli od razu mówi, kiedy pętla ma działać. Dla początkujących często jest łatwiejszy do zrozumienia.

`break` i `continue` są przydatne, ale nie warto używać ich wszędzie. Zbyt wiele takich instrukcji może sprawić, że program będzie trudniejszy do czytania.

## Przykład z szukaniem liczby

```python
szukana = 8

for liczba in range(1, 21):
    print("Sprawdzam liczbę:", liczba)

    if liczba == szukana:
        print("Znaleziono:", liczba)
        break
```

Omówienie:

1. Program szuka liczby 8.
2. Pętla przechodzi przez liczby od 1 do 20.
3. Po znalezieniu liczby program wypisuje komunikat.
4. `break` przerywa pętlę, bo dalsze sprawdzanie nie jest potrzebne.

## Przykład z pomijaniem niechcianych danych

```python
for liczba in range(1, 11):
    if liczba < 3:
        continue

    print("Przetwarzam liczbę:", liczba)
```

Omówienie:

1. Pętla przechodzi przez liczby od 1 do 10.
2. Liczby mniejsze od 3 są pomijane.
3. Dla liczb 3 i większych program wypisuje komunikat.
4. `continue` pomija tylko obecny obieg, ale pętla działa dalej.

## Typowe błędy uczniów

1. Mylenie `break` i `continue`.
2. Myślenie, że `continue` kończy całą pętlę.
3. Myślenie, że `break` kończy cały program.
4. Użycie `break` poza pętlą.
5. Użycie `continue` poza pętlą.
6. Napisanie `while True` bez `break`.
7. Utworzenie pętli nieskończonej przez `continue` przed zmianą licznika.
8. Nadużywanie `break` zamiast jasnego warunku pętli.
9. Nadużywanie `continue`, przez co kod staje się trudny do czytania.
10. Brak wcięć przy `if`, `break` albo `continue`.

## Ćwiczenia dla ucznia

### A. Zadania proste

1. Napisz pętlę `for`, która wypisuje liczby od 1 do 10, ale przerywa działanie przy liczbie 6.
2. Napisz pętlę `for`, która wypisuje liczby od 1 do 10, ale pomija liczbę 5.
3. Napisz program, który wypisuje liczby od 1 do 20 i pomija liczby parzyste za pomocą `continue`.
4. Napisz program, który pyta o hasło i kończy pętlę po wpisaniu `"python"` za pomocą `break`.
5. Napisz pętlę `while`, która wypisuje liczby od 1 do 10, ale przerywa działanie przy liczbie 7.

### B. Zadania średnie

1. Napisz program, w którym użytkownik wpisuje liczby. Program kończy działanie, gdy użytkownik wpisze 0.
2. Napisz program, który wypisuje liczby od 1 do 30, ale pomija liczby podzielne przez 3.
3. Napisz program, który wczytuje 5 liczb. Jeśli liczba jest ujemna, pomija ją za pomocą `continue`.
4. Napisz program, który szuka liczby 8 w zakresie od 1 do 20 i przerywa pętlę po jej znalezieniu.
5. Napisz program, który pyta o hasło kilka razy i kończy działanie po wpisaniu poprawnego hasła.

### C. Zadania trochę trudniejsze

1. Napisz program, w którym użytkownik wpisuje liczby dodatnie. Program sumuje je i kończy działanie po wpisaniu 0.
2. Napisz program, który wczytuje 10 liczb i sumuje tylko liczby dodatnie. Liczby ujemne pomija za pomocą `continue`.
3. Napisz program, który sprawdza liczby od 1 do `n` i pomija liczby podzielne przez 2 lub przez 3.
4. Napisz program, który pyta o hasło i kończy działanie po 3 błędnych próbach.
5. Napisz program, który wypisuje liczby od 1 do 100, ale kończy działanie, gdy suma wypisanych liczb przekroczy 200.

## Kryteria zaliczenia

Programy są zaliczone, jeżeli:

1. poprawnie używają `break` albo `continue`,
2. instrukcje `break` i `continue` znajdują się wewnątrz pętli,
3. program nie tworzy przypadkowej pętli nieskończonej,
4. wyniki są wypisane w czytelny sposób,
5. uczeń potrafi wyjaśnić różnicę między `break` i `continue`.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.

Każde zadanie może być zapisane w osobnym pliku `.py` albo wyraźnie oddzielone w notebooku.

Proponowane nazwy plików:

```text
break_continue_a01.py
break_continue_b01.py
break_continue_c01.py
```
