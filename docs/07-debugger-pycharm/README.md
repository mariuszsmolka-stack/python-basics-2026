# 07. Debugowanie w PyCharm

Ten dział dotyczy wyłącznie debugowania programów w PyCharm. Ćwiczenia wykonujemy w zwykłych plikach `.py`, uruchamianych w PyCharm.

## Czym jest błąd programu?

Błąd programu to sytuacja, w której program działa inaczej, niż oczekujemy. Czasem program od razu się zatrzymuje i pokazuje komunikat błędu. Czasem działa do końca, ale daje zły wynik.

## Czym jest debugowanie?

Debugowanie to spokojne sprawdzanie, co dzieje się w programie krok po kroku. Debugger nie naprawia programu automatycznie. Pomaga znaleźć miejsce, w którym działanie programu różni się od naszego przewidywania.

Debugger pozwala:

- zatrzymać program w wybranym miejscu,
- wykonywać kod krok po kroku,
- oglądać aktualne wartości zmiennych,
- sprawdzić, która instrukcja zostanie wykonana jako następna,
- porównać przewidywania z rzeczywistym działaniem programu.

## Debug a zwykłe uruchomienie programu

Przy zwykłym uruchomieniu program wykonuje się od początku do końca. Widzimy dopiero wynik końcowy albo komunikat błędu.

Przy uruchomieniu w debuggerze możemy zatrzymać program w środku działania. Dzięki temu widzimy, jak zmieniają się zmienne i która instrukcja powoduje problem.

## Dlaczego najpierw przewidujemy wynik?

Debugger jest najbardziej przydatny wtedy, gdy najpierw myślimy samodzielnie. Przed wykonaniem instrukcji warto zadać pytanie:

Co powinno się teraz zmienić?

Potem wykonujemy jeden krok i sprawdzamy, czy program zrobił to, czego oczekiwaliśmy.

## Jak będziemy pracować?

W każdej lekcji stosujemy prostą kolejność:

1. Co chcemy sprawdzić?
2. Gdzie zatrzymamy program?
3. Jakiej wartości spodziewamy się przed wykonaniem instrukcji?
4. Wykonujemy jeden krok.
5. Porównujemy przewidywanie z rzeczywistą wartością.
6. Wyciągamy wniosek.

## Podstawowe operacje w debuggerze PyCharm

Skróty odnoszą się do domyślnej konfiguracji PyCharm na Windows. Można je zmienić w ustawieniach programu.

| Operacja | Znaczenie | Skrót |
| --- | --- | --- |
| Debug | uruchomienie programu w debuggerze | zależny od konfiguracji |
| Resume Program | kontynuowanie programu | `F9` |
| Step Over | wykonanie bieżącej instrukcji bez wchodzenia do funkcji | `F8` |
| Step Into | wejście do wywoływanej funkcji | `F7` |
| Step Out | opuszczenie aktualnej funkcji | `Shift+F8` |
| Stop | zakończenie debugowania | `Ctrl+F2` |

## Lekcje

1. [Pierwsza sesja debugowania](01-pierwsza-sesja-debugowania.md)
2. [Wykonywanie krok po kroku](02-wykonywanie-krok-po-kroku.md)
3. [Zmienne i Watches](03-zmienne-i-watches.md)
4. [Warunki i pętle](04-warunki-i-petle.md)
5. [Debugowanie funkcji](05-debugowanie-funkcji.md)
6. [Debugowanie algorytmów](06-debugowanie-algorytmow.md)
7. [Ćwiczenia podsumowujące](07-cwiczenia-podsumowujace.md)
