# Gra - zgadywanie liczby

## Cel projektu

Celem projektu jest napisanie prostej gry tekstowej, w której użytkownik zgaduje tajną liczbę.

Projekt pozwala przećwiczyć `input()`, konwersję typów, operatory porównania, `if`, `elif`, `else`, pętlę `while` oraz licznik prób.

## Co program ma robić

Program przechowuje tajną liczbę. Użytkownik próbuje ją odgadnąć.

Po każdej próbie program informuje, czy podana liczba jest za mała, za duża, czy poprawna.

Na końcu program wypisuje liczbę prób.

## Wymagania funkcjonalne

Program ma:

- wypisać tytuł gry,
- mieć tajną liczbę,
- zapytać użytkownika o liczbę,
- powtarzać pytanie tak długo, aż użytkownik odgadnie liczbę,
- wypisać `Za mało.`, jeśli podana liczba jest mniejsza od tajnej,
- wypisać `Za dużo.`, jeśli podana liczba jest większa od tajnej,
- wypisać `Brawo! To poprawna liczba.`, jeśli użytkownik zgadł,
- policzyć liczbę prób,
- po zakończeniu gry wypisać liczbę prób.

## Wymagania techniczne

W projekcie używamy:

- zmiennych,
- `print()`,
- `input()`,
- `int()`,
- operatorów porównania,
- `if`, `elif`, `else`,
- pętli `while`,
- licznika.

W projekcie nie używamy:

- list,
- funkcji własnych,
- klas,
- plików.

Biblioteki `random` można użyć tylko w wersji rozszerzonej.

## Przykładowe działanie programu

```text
Gra: zgadywanie liczby
Zgadnij liczbę od 1 do 10.
Podaj liczbę: 4
Za mało.
Podaj liczbę: 9
Za dużo.
Podaj liczbę: 7
Brawo! To poprawna liczba.
Liczba prób: 3
```

## Wersja podstawowa

W wersji podstawowej tajna liczba jest wpisana na stałe.

```python
tajna_liczba = 7
proba = 0
liczba_prob = 0

print("Gra: zgadywanie liczby")
print("Zgadnij liczbę od 1 do 10.")

while proba != tajna_liczba:
    proba = int(input("Podaj liczbę: "))
    liczba_prob += 1

    if proba < tajna_liczba:
        print("Za mało.")
    elif proba > tajna_liczba:
        print("Za dużo.")
    else:
        print("Brawo! To poprawna liczba.")

print("Liczba prób:", liczba_prob)
```

## Omówienie kodu

`tajna_liczba = 7` zapisuje liczbę, którą użytkownik ma odgadnąć.

`proba = 0` ustawia początkową wartość próby. Wybieramy `0`, bo tajna liczba jest z zakresu od `1` do `10`, więc na początku próba na pewno nie jest poprawna.

`liczba_prob = 0` tworzy licznik prób. Na początku użytkownik nie wykonał jeszcze żadnej próby.

Pierwsze dwa `print()` wypisują tytuł gry i krótką instrukcję.

`while proba != tajna_liczba:` oznacza: powtarzaj pętlę dopóki próba jest różna od tajnej liczby.

`proba = int(input("Podaj liczbę: "))` wczytuje liczbę od użytkownika i zamienia tekst na liczbę całkowitą.

`liczba_prob += 1` oznacza: zwiększ licznik prób o `1`.

Instrukcje `if`, `elif`, `else` wybierają jeden z trzech komunikatów.

Jeśli próba jest za mała, program wypisuje `Za mało.`.

Jeśli próba jest za duża, program wypisuje `Za dużo.`.

Jeśli próba nie jest ani za mała, ani za duża, oznacza to poprawną odpowiedź.

Po odgadnięciu liczby warunek `proba != tajna_liczba` staje się fałszywy i pętla się kończy.

Ostatni `print()` wypisuje liczbę prób po zakończeniu gry.

## Jak czytać ten program?

Dopóki podana próba nie jest równa tajnej liczbie, pytaj użytkownika o kolejną liczbę. Po każdej próbie sprawdź, czy liczba jest za mała, za duża, czy poprawna.

To działa jak zabawa w zgadywanie liczby z kolegą. Jedna osoba zna liczbę, a druga zgaduje. Po każdej próbie dostaje podpowiedź: za mało albo za dużo. Dzięki temu może zbliżyć się do odpowiedzi.

## Etapy wykonania projektu

1. Utwórz plik projektu.
2. Wypisz tytuł gry.
3. Utwórz zmienną `tajna_liczba`.
4. Utwórz zmienną `proba`.
5. Utwórz zmienną `liczba_prob`.
6. Napisz pętlę `while`.
7. W pętli wczytaj liczbę od użytkownika.
8. Zwiększ licznik prób.
9. Dodaj `if` sprawdzający, czy liczba jest za mała.
10. Dodaj `elif` sprawdzający, czy liczba jest za duża.
11. Dodaj `else` dla poprawnej odpowiedzi.
12. Po pętli wypisz liczbę prób.
13. Przetestuj program dla kilku wartości.

## Podpowiedzi

Do wczytania liczby użyj `int(input(...))`.

Pętla `while` pozwala powtarzać pytanie.

Operator `!=` oznacza różne od.

Licznik prób zaczyna się od `0`.

Po każdej próbie wykonaj `liczba_prob += 1`.

`if` / `elif` / `else` pozwala wybrać jeden z trzech komunikatów.

Tajna liczba w wersji podstawowej może być wpisana na stałe.

## Wersja rozszerzona - losowanie liczby

W wersji rozszerzonej komputer może sam wylosować tajną liczbę.

```python
import random

tajna_liczba = random.randint(1, 10)
```

`import random` pozwala użyć losowania.

`random.randint(1, 10)` losuje liczbę całkowitą od `1` do `10`.

Reszta programu może działać tak samo.

Pełny przykład:

```python
import random

tajna_liczba = random.randint(1, 10)
proba = 0
liczba_prob = 0

print("Gra: zgadywanie liczby")
print("Zgadnij liczbę od 1 do 10.")

while proba != tajna_liczba:
    proba = int(input("Podaj liczbę: "))
    liczba_prob += 1

    if proba < tajna_liczba:
        print("Za mało.")
    elif proba > tajna_liczba:
        print("Za dużo.")
    else:
        print("Brawo! To poprawna liczba.")

print("Liczba prób:", liczba_prob)
```

## Wersja rozszerzona - ograniczona liczba prób

W tej wersji użytkownik ma maksymalnie `5` prób. Program kończy się, gdy użytkownik zgadnie liczbę albo gdy wykorzysta wszystkie próby.

Nie używamy `break`. Robimy to za pomocą warunku w pętli `while`.

```python
while proba != tajna_liczba and liczba_prob < 5:
```

Pętla działa dopóki liczba nie została odgadnięta oraz dopóki liczba prób jest mniejsza niż `5`.

Gdy jeden z tych warunków przestaje być spełniony, pętla się kończy.

Przykład:

```python
tajna_liczba = 7
proba = 0
liczba_prob = 0

print("Gra: zgadywanie liczby")
print("Masz maksymalnie 5 prób.")

while proba != tajna_liczba and liczba_prob < 5:
    proba = int(input("Podaj liczbę: "))
    liczba_prob += 1

    if proba < tajna_liczba:
        print("Za mało.")
    elif proba > tajna_liczba:
        print("Za dużo.")
    else:
        print("Brawo! To poprawna liczba.")

if proba == tajna_liczba:
    print("Wygrana.")
else:
    print("Koniec prób.")

print("Liczba prób:", liczba_prob)
```

## Co uczeń ma dodać od siebie?

Do projektu dodaj minimum 5 samodzielnych zmian.

Co najmniej jedna zmiana musi wpływać na działanie programu, a nie tylko na tekst komunikatów.

Nie musisz wymyślać wszystkich zmian samodzielnie. Możesz wybrać propozycje z listy, ale program ma być spójny i działać poprawnie.

## Przykłady zmian, które możesz dodać

1. Inny zakres liczb

Zamiast zgadywania od `1` do `10`, program może działać w zakresie od `1` do `20` albo od `1` do `100`.

Przykład komunikatu:

```text
Zgadnij liczbę od 1 do 20.
```

2. Inna tajna liczba

W wersji bez losowania uczeń zmienia tajną liczbę na własną, na przykład:

```python
tajna_liczba = 13
```

3. Limit prób

Program pozwala na maksymalnie `5` prób.

Jeżeli użytkownik nie zgadnie, program wypisuje komunikat o przegranej.

4. Ocena wyniku

Po zakończeniu gry program ocenia wynik:

- `1-2` próby: `Świetny wynik!`
- `3-5` prób: `Dobry wynik.`
- więcej niż `5` prób: `Udało się, ale można szybciej.`

5. Komunikat powitalny

Program wypisuje krótki opis zasad gry przed rozpoczęciem.

6. Komunikat po każdej próbie

Program wypisuje numer aktualnej próby, na przykład:

```text
To była próba numer 3.
```

7. Bardziej przyjazne podpowiedzi

Zamiast tylko `Za mało.` albo `Za dużo.`, program może wypisywać:

- `Za mało. Spróbuj podać większą liczbę.`
- `Za dużo. Spróbuj podać mniejszą liczbę.`

8. Podsumowanie gry

Po zakończeniu program wypisuje tajną liczbę, liczbę prób i komunikat końcowy.

9. Wersja z losowaniem

Dla chętnych program może losować liczbę:

```python
import random
tajna_liczba = random.randint(1, 20)
```

10. Komentarze w kodzie

Uczeń dodaje krótkie komentarze wyjaśniające pętlę i licznik prób, na przykład:

```python
# Pętla działa, dopóki użytkownik nie odgadnie liczby
while proba != tajna_liczba:
```

## Przykładowy zestaw zmian dla ucznia

Uczeń może wybrać na przykład taki zestaw 5 zmian:

1. Zmienić tytuł gry.
2. Zmienić zakres zgadywania na 1-20.
3. Dodać limit 5 prób.
4. Dodawać komunikat z numerem próby.
5. Dodać podsumowanie gry po zakończeniu.

Drugi przykładowy zestaw:

1. Zmienić komunikaty dla użytkownika.
2. Zmienić tajną liczbę.
3. Dodać ocenę wyniku zależną od liczby prób.
4. Dodać bardziej przyjazne podpowiedzi.
5. Dodać komentarz wyjaśniający działanie pętli `while`.

Trzeci przykładowy zestaw dla chętnych:

1. Dodać losowanie liczby.
2. Zmienić zakres losowania na 1-50.
3. Dodać limit prób.
4. Dodać komunikat o przegranej po wykorzystaniu wszystkich prób.
5. Dodać końcowe podsumowanie gry.

## Kryteria zaliczenia

Program jest zaliczony, jeżeli:

- uruchamia się bez błędów,
- wypisuje tytuł gry,
- ma tajną liczbę,
- wczytuje liczbę od użytkownika,
- używa `int(input(...))`,
- używa pętli `while`,
- używa `if` / `elif` / `else`,
- informuje, czy liczba jest za mała, za duża, czy poprawna,
- kończy działanie po odgadnięciu liczby,
- liczy liczbę prób,
- wypisuje liczbę prób po zakończeniu gry,
- ma czytelne nazwy zmiennych.

## Typowe błędy uczniów

1. Brak konwersji `int()` przy `input()`.
2. Użycie `=` zamiast `==` w warunku.
3. Mylenie `==` oraz `!=`.
4. Brak zmiany wartości zmiennej `proba` w pętli.
5. Brak licznika prób.
6. Zwiększanie licznika prób w złym miejscu.
7. Źle zapisany warunek pętli `while`.
8. Brak dwukropka po `while`, `if`, `elif` albo `else`.
9. Brak wcięć.
10. Użycie kilku oddzielnych `if` zamiast `if` / `elif` / `else`.
11. Stworzenie pętli nieskończonej.
12. Wypisanie liczby prób przed zakończeniem pętli zamiast po pętli.

## Czego nie robić

Nie wpisuj `proba` na stałe zamiast wczytywać jej od użytkownika.

Nie ukrywaj komunikatów dla użytkownika.

Nie używaj nazw zmiennych `x`, `y`, `z`, jeśli możesz użyć `tajna_liczba`, `proba`, `liczba_prob`.

Nie kopiuj kodu bez zrozumienia.

Nie dodawaj list, funkcji ani klas do wersji podstawowej.

## Sposób oddania pracy

Uczeń zapisuje projekt w swoim folderze w JupyterLab.

Nazwa pliku:

```text
projekt_03_zgadywanie_liczby.py
```

Uczeń może najpierw testować rozwiązanie w notebooku, ale ostateczna wersja powinna być zapisana jako plik `.py`.
