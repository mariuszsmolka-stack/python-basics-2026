# Wykonywanie krok po kroku

## Cel lekcji

Nauczysz się wykonywać program po jednej instrukcji i obserwować, jak zmienia się wartość zmiennej.

## Program do ćwiczenia

Utwórz plik `.py`:

```python
wynik = 10
wynik = wynik + 5
wynik = wynik * 2
wynik = wynik - 4
print(wynik)
```

## Bieżące miejsce wykonania

W debuggerze PyCharm wyróżniony wiersz oznacza instrukcję, która czeka na wykonanie. To ważne: jeśli wiersz jest podświetlony, to zwykle nie został jeszcze wykonany.

Instrukcji wykonanej nie można cofnąć. Jeśli chcesz zacząć od początku, zatrzymaj debugowanie i uruchom program ponownie.

## Step Over, Resume Program i Stop

- `Step Over` (`F8`) wykonuje bieżącą instrukcję i zatrzymuje program na następnej.
- `Resume Program` (`F9`) kontynuuje program do kolejnego punktu przerwania albo do końca.
- `Stop` (`Ctrl+F2`) kończy debugowanie.

## Praca krok po kroku

1. Co chcemy sprawdzić?
   Chcemy sprawdzić, jak zmienia się `wynik`.
2. Gdzie zatrzymamy program?
   Ustaw punkt przerwania przy pierwszej instrukcji.
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
   Przed pierwszą instrukcją zmienna `wynik` jeszcze nie ma wartości.
4. Wykonujemy jeden krok.
   Naciśnij `F8`.
5. Porównujemy przewidywanie z rzeczywistą wartością.
   Po pierwszym kroku `wynik` powinien mieć wartość `10`.
6. Wyciągamy wniosek.
   Każdy krok może zmienić wartość zmiennej.

## Tabela obserwacji

| Instrukcja | Przewidywana wartość | Wartość w debuggerze |
| --- | ---: | ---: |
| `wynik = 10` | 10 |  |
| `wynik = wynik + 5` | 15 |  |
| `wynik = wynik * 2` | 30 |  |
| `wynik = wynik - 4` | 26 |  |
| `print(wynik)` | 26 |  |

## Ćwiczenia

1. Ustaw punkt przerwania przy pierwszym wierszu programu.
2. Wykonuj program klawiszem `F8` i uzupełnij tabelę.
3. Użyj `F9` i sprawdź, co stanie się po wznowieniu programu.
4. Zatrzymaj debugowanie skrótem `Ctrl+F2`.
5. Uruchom program ponownie i sprawdź, czy wartości są takie same.
6. Zmień wartość początkową `wynik` na `20` i przewidź nowe wartości.
7. Dodaj jedną instrukcję odejmowania i sprawdź ją w debuggerze.
