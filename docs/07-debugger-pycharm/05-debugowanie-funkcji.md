# Debugowanie funkcji

## Cel lekcji

Nauczysz się sprawdzać działanie funkcji w debuggerze PyCharm.

## Program do ćwiczenia

Utwórz plik `.py`:

```python
def obliczPoleProstokata(dlugosc, szerokosc):
    pole = dlugosc * szerokosc
    return pole


wynik = obliczPoleProstokata(5, 3)
print(wynik)
```

## Step Over, Step Into i Step Out

- `Step Over` (`F8`) wykonuje wywołanie funkcji bez wchodzenia do jej środka.
- `Step Into` (`F7`) wchodzi do wywoływanej funkcji.
- `Step Out` (`Shift+F8`) opuszcza aktualną funkcję i wraca do miejsca wywołania.

## Parametry i zmienne lokalne

Parametry `dlugosc` i `szerokosc` otrzymują wartości przekazane przy wywołaniu funkcji.

Zmienna `pole` jest zmienną lokalną. Widzimy ją podczas wykonywania funkcji. Po powrocie do miejsca wywołania najważniejsza jest wartość zwrócona przez `return`.

## Praca krok po kroku

1. Co chcemy sprawdzić?
   Chcemy sprawdzić, jak funkcja oblicza pole prostokąta.
2. Gdzie zatrzymamy program?
   Ustaw punkt przerwania przy wierszu `wynik = obliczPoleProstokata(5, 3)`.
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
   Spodziewamy się, że funkcja zwróci `15`.
4. Wykonujemy jeden krok.
   Użyj `F7`, aby wejść do funkcji.
5. Porównujemy przewidywanie z rzeczywistą wartością.
   W funkcji parametry powinny mieć wartości `5` i `3`, a `pole` po obliczeniu powinno wynosić `15`.
6. Wyciągamy wniosek.
   Debugger pokazuje drogę od wywołania funkcji do wartości zwracanej przez `return`.

## Powrót z funkcji

Po wykonaniu `return pole` program wraca do wiersza wywołania. Wtedy wynik funkcji trafia do zmiennej `wynik`.

## Ćwiczenia

1. Ustaw punkt przerwania przy wywołaniu funkcji.
2. Użyj `F8` i sprawdź, czy program wykona funkcję bez wchodzenia do środka.
3. Uruchom program ponownie i użyj `F7`, aby wejść do funkcji.
4. Sprawdź wartości `dlugosc`, `szerokosc` i `pole`.
5. Użyj `Shift+F8`, aby opuścić funkcję.
6. Zmień argumenty funkcji na `8` i `4`, a potem przewidź wynik.
7. Dodaj drugie wywołanie funkcji i prześledź oba wywołania.
