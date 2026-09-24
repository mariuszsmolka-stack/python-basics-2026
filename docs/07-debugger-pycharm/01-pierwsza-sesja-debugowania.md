# Pierwsza sesja debugowania

## Cel lekcji

Nauczysz się uruchamiać program w debuggerze PyCharm i zatrzymywać go w wybranym miejscu.

## Run i Debug

`Run` uruchamia program normalnie. Program wykonuje się od początku do końca.

`Debug` uruchamia program w debuggerze. Dzięki temu możemy zatrzymać wykonanie programu na punkcie przerwania i obejrzeć wartości zmiennych.

## Punkt przerwania

Punkt przerwania to miejsce, w którym program ma się zatrzymać. W PyCharm ustawiamy go przez kliknięcie obok numeru wiersza.

Program zatrzymuje się przed wykonaniem wskazanego wiersza. Bieżący wiersz jest wyróżniony. To znaczy, że ta instrukcja dopiero czeka na wykonanie.

## Program do ćwiczenia

Utwórz plik `.py` i wpisz:

```python
cena = 12
liczbaSztuk = 3
koszt = cena * liczbaSztuk
print(koszt)
```

## Praca krok po kroku

1. Co chcemy sprawdzić?
   Chcemy sprawdzić, kiedy powstaje zmienna `koszt` i jaką ma wartość.
2. Gdzie zatrzymamy program?
   Ustaw punkt przerwania przy wierszu `koszt = cena * liczbaSztuk`.
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
   Przed wykonaniem tego wiersza istnieją już `cena` i `liczbaSztuk`, ale `koszt` jeszcze nie ma obliczonej wartości.
4. Wykonujemy jeden krok.
   Uruchom `Debug`, poczekaj na zatrzymanie programu i wykonaj krok.
5. Porównujemy przewidywanie z rzeczywistą wartością.
   Po wykonaniu wiersza `koszt` powinien mieć wartość `36`.
6. Wyciągamy wniosek.
   Debugger pokazuje, w którym momencie zmienna otrzymuje wartość.

## Okno Debug

Po uruchomieniu programu poleceniem `Debug` w PyCharm pojawia się okno `Debug`. Widać w nim między innymi:

- bieżące miejsce zatrzymania programu,
- wartości zmiennych,
- przyciski do wykonywania kolejnych kroków,
- przycisk zakończenia debugowania.

## Zakończenie debugowania

Aby zakończyć sesję debugowania, użyj `Stop` albo skrótu `Ctrl+F2`.

## Ćwiczenia

1. Uruchom program normalnie za pomocą `Run` i zapisz wynik.
2. Ustaw punkt przerwania przy wierszu obliczającym `koszt`.
3. Uruchom program poleceniem `Debug`.
4. Sprawdź wartości `cena`, `liczbaSztuk` i `koszt` przed oraz po wykonaniu obliczenia.
5. Zmień `liczbaSztuk` na `5` i powtórz debugowanie.
6. Zakończ debugowanie skrótem `Ctrl+F2`.
