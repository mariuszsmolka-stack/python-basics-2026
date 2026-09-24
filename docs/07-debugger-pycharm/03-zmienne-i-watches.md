# Zmienne i Watches

## Cel lekcji

Nauczysz się obserwować wartości zmiennych w panelu `Variables` i dodawać proste wyrażenia do `Watches`.

## Program do ćwiczenia

Utwórz plik `.py`:

```python
liczby = [4, 7, 2]
suma = 0
suma = suma + liczby[0]
suma = suma + liczby[1]
suma = suma + liczby[2]
print(suma)
```

## Panel Variables

Panel `Variables` pokazuje aktualne wartości zmiennych. W PyCharm niektóre wartości mogą być też widoczne obok kodu.

Listę można rozwinąć, aby zobaczyć jej elementy. Dla zmiennej `liczby` zobaczysz wartości pod indeksami `0`, `1` i `2`.

## Watches

`Watches` pozwala obserwować wybrane zmienne albo proste wyrażenia.

W tym programie możesz obserwować:

- `suma`,
- `liczby`,
- `len(liczby)`,
- `liczby[0]`.

Po każdym kroku wartości w `Variables` i `Watches` mogą się zmienić.

## Praca krok po kroku

1. Co chcemy sprawdzić?
   Chcemy sprawdzić, jak rośnie `suma`.
2. Gdzie zatrzymamy program?
   Ustaw punkt przerwania przy wierszu `suma = 0`.
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
   Przed wykonaniem tej instrukcji `suma` jeszcze nie ma wartości.
4. Wykonujemy jeden krok.
   Naciśnij `F8`.
5. Porównujemy przewidywanie z rzeczywistą wartością.
   Po wykonaniu instrukcji `suma` powinna mieć wartość `0`.
6. Wyciągamy wniosek.
   Debugger pokazuje, kiedy zmienna powstaje i kiedy zmienia wartość.

## Tabela obserwacji

| Krok | Instrukcja | Przewidywana wartość `suma` | Wartość w debuggerze |
| --- | --- | ---: | ---: |
| 1 | `suma = 0` | 0 |  |
| 2 | `suma = suma + liczby[0]` | 4 |  |
| 3 | `suma = suma + liczby[1]` | 11 |  |
| 4 | `suma = suma + liczby[2]` | 13 |  |

## Ćwiczenia

1. Uruchom program w debuggerze i obserwuj `suma`.
2. Rozwiń listę `liczby` w panelu `Variables`.
3. Dodaj do `Watches` wyrażenie `len(liczby)`.
4. Dodaj do `Watches` wyrażenie `liczby[0]`.
5. Zmień liczby w liście i przewidź nową wartość sumy.
6. Wykonuj program krok po kroku i uzupełnij tabelę.
7. Dodaj czwarty element do listy i dopisz instrukcję dodawania.
