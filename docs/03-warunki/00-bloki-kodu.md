# Bloki kodu i wcięcia w Pythonie

## Cel lekcji

Poznasz bloki kodu i dowiesz się, dlaczego wcięcia w Pythonie są częścią składni.

## Czego się nauczysz

Po tej lekcji będziesz umieć rozpoznać, które instrukcje należą do bloku kodu. Zrozumiesz też, dlaczego po dwukropku musi pojawić się wcięty kod i co oznacza błąd `IndentationError`.

## Czym jest blok kodu

Blok kodu to grupa instrukcji, które należą do jednej konstrukcji programu, na przykład do `if`, `else`, `while` albo `for`.

W Pythonie blok kodu poznajemy po wcięciu.

Wcięcie to przesunięcie kodu w prawo. Najczęściej robimy je za pomocą 4 spacji.

## Python rozpoznaje bloki po wcięciach

W wielu językach programowania wcięcia pomagają tylko w czytaniu kodu. W Pythonie jest inaczej.

W Pythonie wcięcia są częścią składni. To znaczy, że Python używa ich do zrozumienia programu.

Jeśli wcięcie jest złe, program może działać inaczej albo Python zgłosi błąd.

## Przykład bloku przy if

```python
wiek = int(input("Podaj wiek: "))

if wiek >= 18:
    print("Jesteś osobą pełnoletnią.")
    print("Możesz przejść dalej.")

print("Koniec programu.")
```

Omówienie:

Dwie instrukcje `print()` z wcięciem należą do bloku `if`.

Wykonają się tylko wtedy, gdy warunek `wiek >= 18` jest prawdziwy.

Ostatni `print()` nie ma wcięcia.

Dlatego nie należy już do bloku `if`.

Ostatni `print()` wykona się zawsze.

## Dwukropek i wcięcie zawsze razem

W Pythonie po konstrukcjach takich jak `if`, `elif`, `else`, `while` i `for` stawiamy dwukropek.

Dwukropek oznacza, że za chwilę zacznie się blok kodu.

Po dwukropku musi pojawić się przynajmniej jedna instrukcja z wcięciem.

Poprawny przykład:

```python
if liczba > 0:
    print("Liczba jest dodatnia.")
```

Błędny przykład:

```python
if liczba > 0:
print("Liczba jest dodatnia.")
```

Po dwukropku powinno być wcięcie. Tutaj go brakuje. Python zgłosi błąd wcięcia.

Drugi błędny przykład:

```python
if liczba > 0:

print("Koniec.")
```

Po dwukropku nie ma żadnej instrukcji należącej do `if`.

Pusty blok jest błędem.

Python oczekuje przynajmniej jednej wciętej instrukcji.

## Co zrobić, gdy blok ma być chwilowo pusty?

Jeśli blok ma być chwilowo pusty, można użyć instrukcji `pass`.

```python
if liczba > 0:
    pass

print("Koniec programu.")
```

`pass` oznacza: nic nie rób.

Używamy go czasem tymczasowo.

Dzięki `pass` blok nie jest pusty.

Później zamiast `pass` można dopisać właściwy kod.

Ważne: `pass` nie jest rozwiązaniem zadania. To tylko tymczasowy wypełniacz pustego bloku.

## Kiedy w Pythonie występują bloki kodu?

Na poziomie tego kursu bloki kodu występują przede wszystkim przy:

- `if`,
- `elif`,
- `else`,
- `while`,
- `for`.

Krótkie przykłady:

```python
if warunek:
    instrukcja
```

```python
elif inny_warunek:
    instrukcja
```

```python
else:
    instrukcja
```

```python
while warunek:
    instrukcja
```

```python
for i in range(5):
    instrukcja
```

W dalszej nauce bloki pojawią się też przy funkcjach, klasach i innych konstrukcjach, ale w tym kursie najważniejsze są bloki przy warunkach i pętlach.

## Kiedy blok się kończy?

Blok kończy się wtedy, gdy kod wraca do wcześniejszego poziomu wcięcia.

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("To jest blok if.")
    print("Ten wiersz też należy do if.")

print("Ten wiersz jest już poza blokiem if.")
```

Dwa pierwsze `print()` są wcięte.

Należą do `if`.

Ostatni `print()` nie jest wcięty.

Dlatego jest poza blokiem `if`.

## Kod w bloku i kod poza blokiem

Kod w bloku wykonuje się zgodnie z zasadami danej konstrukcji.

Na przykład kod w bloku `if` wykona się tylko wtedy, gdy warunek jest prawdziwy.

Kod poza blokiem nie należy już do tej konstrukcji.

Dlatego może wykonać się zawsze albo w innym momencie programu.

## Ile spacji używać?

W Pythonie standardowo używa się 4 spacji na jedno wcięcie.

Najważniejsze jest to, aby w jednym bloku wcięcia były równe.

Przykład poprawny:

```python
if liczba > 0:
    print("Pierwsza instrukcja")
    print("Druga instrukcja")
```

Przykład błędny:

```python
if liczba > 0:
    print("Pierwsza instrukcja")
  print("Druga instrukcja")
```

Instrukcje w tym samym bloku muszą mieć takie samo wcięcie.

Nierówne wcięcia powodują błąd albo zmieniają sens programu.

## Blok przy if-else

```python
liczba = int(input("Podaj liczbę: "))

if liczba % 2 == 0:
    print("Liczba jest parzysta.")
else:
    print("Liczba jest nieparzysta.")

print("Sprawdzanie zakończone.")
```

`if` ma swój blok.

`else` ma swój blok.

Oba bloki są wcięte.

Końcowy `print()` jest poza `if-else` i wykona się zawsze.

## Przykład bloku przy elif

```python
temperatura = float(input("Podaj temperaturę: "))

if temperatura > 30:
    print("Gorąco.")
elif temperatura > 20:
    print("Ciepło.")
else:
    print("Chłodno albo zimno.")
```

Każda część ma własny blok.

Blok pod `elif` wykona się tylko wtedy, gdy wcześniejszy warunek był fałszywy, a warunek przy `elif` jest prawdziwy.

## Blok przy pętli while

```python
licznik = 1

while licznik <= 3:
    print("Licznik:", licznik)
    licznik += 1

print("Koniec pętli.")
```

Dwie instrukcje z wcięciem należą do pętli.

Będą powtarzane.

Ostatni `print()` nie jest wcięty.

Wykona się dopiero po zakończeniu pętli.

## Blok przy pętli for

```python
for i in range(3):
    print("Obieg pętli:", i)

print("Koniec.")
```

`print()` z wcięciem należy do pętli `for`.

Wykona się kilka razy.

`print()` bez wcięcia jest poza pętlą.

Wykona się raz po zakończeniu pętli.

## Typowe błędy uczniów

1. Brak dwukropka po `if`, `elif`, `else`, `while` albo `for`.
2. Brak wcięcia po dwukropku.
3. Pusty blok po dwukropku.
4. Nierówne wcięcia w tym samym bloku.
5. Mylenie kodu w bloku z kodem poza blokiem.
6. Wypisanie wyniku końcowego wewnątrz pętli zamiast po pętli.
7. Przypadkowe przesunięcie jednej linii kodu.
8. Używanie tabulatorów i spacji jednocześnie.
9. Myślenie, że wcięcia są tylko dla wyglądu.
10. Dopisywanie `else` bez pasującego `if`.

## Najważniejsza zasada

Jeżeli w Pythonie stawiasz dwukropek po `if`, `elif`, `else`, `while` albo `for`, to następna część programu musi tworzyć blok kodu. Blok kodu musi mieć wcięcie i musi zawierać przynajmniej jedną instrukcję.

## Ćwiczenia

1. Przepisz poprawny przykład z `if` i zaznacz, które linie należą do bloku.
2. Popraw program, w którym po `if` brakuje wcięcia.
3. Popraw program, w którym po `else` brakuje wcięcia.
4. Popraw program, w którym blok `if` jest pusty.
5. Dopisz instrukcję `pass` do pustego bloku, a potem zamień `pass` na prawdziwy kod.
6. Napisz program z `if`, w którym jeden `print()` jest w bloku, a drugi poza blokiem.
7. Napisz program z `while`, w którym wynik końcowy wypisuje się po pętli.
8. Napisz program z `for`, w którym jeden komunikat wypisuje się w pętli, a drugi po pętli.
9. Wyjaśnij własnymi słowami, kiedy kończy się blok kodu.
10. Znajdź błąd w programie z nierównymi wcięciami i popraw go.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
