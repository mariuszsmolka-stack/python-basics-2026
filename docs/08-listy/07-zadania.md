---
layout: default
title: Samodzielne zadania - listy
---

# Samodzielne zadania - listy

Wykonaj każde zadanie jako osobny program. Korzystaj z konstrukcji poznanych w lekcjach 01-06 oraz z wcześniejszych lekcji o zmiennych, warunkach i pętlach. Stosuj polskie nazwy zmiennych w konwencji camelCase.

W zadaniach z odczytem zakładamy poprawny zapis liczb. Liczba wczytywanych elementów jest nieujemna. Danych błędnych, takich jak litery zamiast liczby, nie trzeba obsługiwać. Pustą listę obsłuż tam, gdzie zadanie tego wymaga.

Nie używaj funkcji własnych, klas, plików, słowników, zbiorów, list składanych ani bibliotek. Przed uruchomieniem programu przewiduj wyniki. Sprawdzaj także powtórzenia, zero i liczby ujemne, jeśli mieszczą się w danych zadania.

## A. Zadania podstawowe - 8 zadań

### Zadanie 1. Pierwsza lista ocen

Utwórz listę zawierającą oceny `3`, `4`, `5`, `2`, dokładnie w tej kolejności. Wypisz całą listę w jednym wierszu. Program nie pobiera danych od użytkownika.

Oczekiwany wynik: `[3, 4, 5, 2]`.

### Zadanie 2. Lista imion

Przygotuj dane: `Ala`, `Olek`, `Maja`. Wypisz je jako jedną listę napisów. Nie wypisuj imion w oddzielnych wierszach.

Wynik ma zawierać trzy elementy w podanej kolejności: `['Ala', 'Olek', 'Maja']`.

### Zadanie 3. Wybrane elementy

Dane to lista `[12, 7, 19, 4, 10]`. Wypisz pierwszy, trzeci i ostatni element, każdy w osobnym wierszu. Nie zmieniaj listy.

Oczekiwane wartości: kolejno `12`, `19`, `10`.

### Zadanie 4. Poprawienie wyniku

Dane to `[5, 8, 3, 9]`. Zmień drugi element na `10`. Pozostałe elementy i długość listy mają zostać bez zmian. Wypisz listę po zmianie.

Oczekiwany wynik: `[5, 10, 3, 9]`.

### Zadanie 5. Nowy produkt

Dane to lista napisów `['chleb', 'mleko']`. Dopisz na końcu napis `ser`. Wypisz końcową listę. Nie zastępuj żadnego z dotychczasowych produktów.

Oczekiwany wynik: `['chleb', 'mleko', 'ser']`.

### Zadanie 6. Usunięta pozycja

Dane to `[4, 9, 6, 2]`. Usuń element z indeksem `1`. Wypisz usuniętą wartość, a potem pozostałą listę, w osobnych wierszach.

Oczekiwane wyniki: `9` oraz `[4, 6, 2]`.

### Zadanie 7. Ile pomiarów?

Dane to `[0, 2, 0, -1, 2]`. Wypisz liczbę elementów. Powtórzenia i zero również są elementami.

Dla tych danych wynik to `5`. Sprawdź również pustą listę: oczekiwany wynik to `0`.

### Zadanie 8. Każda wartość osobno

Dane to `[6, 2, 8, 2]`. Wypisz wszystkie elementy w osobnych wierszach za pomocą pętli. Zachowaj kolejność i powtórzenia. Nie wypisuj indeksów.

Oczekiwane cztery wiersze zawierają kolejno `6`, `2`, `8`, `2`.

## B. Zadania średnie - 8 zadań

### Zadanie 9. Suma wartości

Dane to `[4, -2, 7, 0, 3]`. Oblicz sumę elementów za pomocą pętli, bez funkcji `sum()`. Wypisz jeden wynik.

Oczekiwany wynik: `12`. Dla pustej listy program ma wypisać `0`.

### Zadanie 10. Średnia bez błędu

Dane to `[2, 4, 6, 8]`. Wypisz średnią arytmetyczną elementów. Sprawdź również pustą listę. Wtedy zamiast obliczenia ma pojawić się komunikat `Brak danych`.

Dla podanych czterech liczb oczekiwany wynik to `5.0`.

### Zadanie 11. Najmniejsza i największa

Dane to `[-8, -2, -5]`. Wypisz najmniejszą i największą wartość, każdą w osobnym wierszu. Możesz korzystać z funkcji wbudowanych.

Oczekiwane wartości: `-8` i `-2`. Dla pustej listy wypisz tylko `Brak danych`.

### Zadanie 12. Liczba wystąpień

Dane to `[3, 5, 3, 2, 3, 5]`. Wczytaj jedną liczbę całkowitą. Wypisz, ile razy występuje w liście. Nie zmieniaj danych.

Dla odczytu `3` wynik to `3`. Dla odczytu `7` wynik to `0`.

### Zadanie 13. Wyniki ponad progiem

Dane to `[8, 12, 10, 4, 16, 10]`. Policz, ile elementów ma wartość co najmniej `10`. Wypisz samą liczbę takich elementów. Nie obliczaj ich sumy.

Oczekiwany wynik: `4`.

### Zadanie 14. Czy wartość występuje?

Dane to `[7, 2, 9, 2]`. Wczytaj liczbę całkowitą. Wypisz `Znaleziono`, gdy występuje w liście, albo `Nie znaleziono`, gdy jej nie ma. Program ma wypisać jeden komunikat, niezależnie od liczby powtórzeń.

Dla odczytu `2` oczekiwany wynik to `Znaleziono`. Dla odczytu `5` - `Nie znaleziono`.

### Zadanie 15. Lista z danych wejściowych

W pierwszym wierszu wczytaj liczbę elementów, a w kolejnych wierszach tyle liczb całkowitych. Zapisz liczby w liście. Wypisz całą listę, a następnie jej długość. Liczba elementów nie jest częścią listy.

Przykładowe wejście:

```text
3
8
-2
5
```

Oczekiwany wynik:

```text
[8, -2, 5]
3
```

Dla liczby elementów równej `0` oczekiwane są dwa wiersze: `[]` oraz `0`.

### Zadanie 16. Wartości ujemne na zero

Dane to `[4, -3, 0, -1, 7]`. Zmień każdy ujemny element istniejącej listy na `0`. Pozostałe wartości, ich pozycje i długość listy mają pozostać bez zmian. Wypisz zmodyfikowaną listę.

Oczekiwany wynik: `[4, 0, 0, 0, 7]`.

## C. Zadania trudniejsze - 4 zadania

### Zadanie 17. Podsumowanie ocen

Dane to lista ocen całkowitych od `1` do `6`. Dla listy niepustej wypisz, w tej kolejności:

- liczbę ocen;
- ich średnią;
- liczbę ocen co najmniej równych `4`;
- nową listę ocen uporządkowaną rosnąco.

Lista źródłowa ma zachować początkową kolejność. Dla pustej listy wypisz wyłącznie `Brak ocen`.

Przykładowe dane: `[3, 5, 2, 4, 6]`. Oczekiwane wyniki w kolejnych wierszach:

```text
5
4.0
3
[2, 3, 4, 5, 6]
```

### Zadanie 18. Nieujemne temperatury

Dane to lista temperatur całkowitych. Utwórz nową listę zawierającą wyłącznie temperatury większe lub równe zero. Zachowaj kolejność, powtórzenia i listę źródłową.

Wypisz nową listę, liczbę ujemnych pomiarów w źródle oraz średnią elementów nowej listy. Jeśli nowa lista jest pusta, zamiast średniej wypisz `Brak nieujemnych pomiarów`. Program ma działać również dla pustej listy źródłowej.

Dla danych `[-2, 0, 4, -1, 8]` oczekiwany wynik to:

```text
[0, 4, 8]
2
4.0
```

Dla danych `[-5, -1]` oczekiwany wynik to:

```text
[]
2
Brak nieujemnych pomiarów
```

### Zadanie 19. Korekta punktów

Dane to lista całkowitych wyników punktowych. Przygotuj nową listę tej samej długości. Każda wartość poniżej `0` ma zostać zastąpiona przez `0`, a każda wartość powyżej `100` - przez `100`. Wartości od `0` do `100` włącznie pozostają bez zmian.

Wypisz skorygowaną listę, liczbę zmienionych wartości i listę maksymalnie trzech największych skorygowanych wyników w kolejności malejącej. Zachowaj powtórzenia. Nie zmieniaj źródła. Jeśli wyników jest mniej niż trzy, wypisz wszystkie dostępne. Program ma działać także dla pustej listy.

Dla danych `[105, -4, 60, 100, 0]` oczekiwany wynik to:

```text
[100, 0, 60, 100, 0]
2
[100, 100, 60]
```

Dla pustej listy oczekiwane trzy wiersze to: `[]`, `0`, `[]`.

### Zadanie 20. Porównanie dwóch zestawów

Dane to dwie listy całkowitych wyników: wcześniejsze i późniejsze. Listy mają tę samą długość. Elementy na tej samej pozycji dotyczą tej samej osoby.

Policz, ile osób poprawiło wynik, ile uzyskało ten sam wynik, a ile uzyskało wynik niższy. Wypisz te trzy liczby w podanej kolejności, każdą w osobnym wierszu. Nie zmieniaj ani nie sortuj list. Dla dwóch pustych list wypisz trzy zera.

Przykładowe dane wcześniejsze: `[10, 15, 12, 20]`. Późniejsze: `[12, 15, 8, 25]`.

Oczekiwany wynik:

```text
2
1
1
```
