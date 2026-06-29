# Instrukcja elif w Pythonie - kilka warunków po kolei

## Cel lekcji

Poznasz instrukcję `elif` i nauczysz się sprawdzać kilka warunków po kolei.

## Czego się nauczysz

Po tej lekcji będziesz umieć zapisać program, który wybiera jedną z kilku możliwości. Nauczysz się używać konstrukcji `if-elif-else`, ustawiać warunki w dobrej kolejności i rozumieć, która część kodu się wykona.

## Przypomnienie if oraz if-else

Instrukcja `if` sprawdza jeden warunek.

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
```

Instrukcja `if-else` pozwala wybrać jedną z dwóch możliwości.

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
else:
    print("Liczba nie jest dodatnia.")
```

Gdy mamy więcej niż dwie możliwości, używamy `elif`.

## Po co używamy elif

`elif` oznacza: w przeciwnym razie, jeżeli...

Używamy go wtedy, gdy program ma sprawdzić kilka warunków po kolei.

Python sprawdza warunki od góry do dołu. Gdy znajdzie pierwszy prawdziwy warunek, wykonuje jego część i kończy sprawdzanie całej konstrukcji.

W konstrukcji `if-elif-else` wykonuje się tylko jedna pasująca część.

## Składnia if-elif-else

Podstawowy zapis wygląda tak:

```python
if warunek1:
    instrukcje
elif warunek2:
    instrukcje
elif warunek3:
    instrukcje
else:
    instrukcje
```

`if` sprawdza pierwszy warunek.

`elif` sprawdza kolejny warunek tylko wtedy, gdy wcześniejsze warunki były fałszywe.

`else` wykonuje się wtedy, gdy żaden wcześniejszy warunek nie został spełniony.

`else` nie ma własnego warunku.

Po `if`, `elif` i `else` stawiamy dwukropek `:`.

Instrukcje należące do danej części muszą być wcięte.

## Jak czytać if-elif-else?

Konstrukcję `if-elif-else` można czytać tak:

Jeśli pierwszy warunek jest prawdziwy, wykonaj pierwszą część. W przeciwnym razie, jeżeli drugi warunek jest prawdziwy, wykonaj drugą część. W przeciwnym razie, jeżeli trzeci warunek jest prawdziwy, wykonaj trzecią część. Jeśli żaden warunek nie pasuje, wykonaj `else`.

Ważne: Python zatrzymuje się przy pierwszym spełnionym warunku.

## Ocena na podstawie punktów

```python
punkty = int(input("Podaj liczbę punktów: "))

if punkty >= 90:
    print("Ocena bardzo dobra")
elif punkty >= 75:
    print("Ocena dobra")
elif punkty >= 50:
    print("Ocena dostateczna")
else:
    print("Brak zaliczenia")
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje liczbę punktów.

Najpierw program sprawdza, czy punktów jest co najmniej `90`.

Jeśli tak, wypisuje ocenę bardzo dobrą i kończy sprawdzanie całej konstrukcji.

Jeśli nie, sprawdza kolejny warunek.

Jeśli punktów jest co najmniej `75`, wypisuje ocenę dobrą.

Jeśli nie, sprawdza kolejny warunek.

Jeśli punktów jest co najmniej `50`, wypisuje ocenę dostateczną.

Jeśli żaden warunek nie pasuje, wykonuje się `else`.

## Przykład z temperaturą

```python
temperatura = float(input("Podaj temperaturę: "))

if temperatura > 30:
    print("Jest bardzo gorąco.")
elif temperatura > 20:
    print("Jest ciepło.")
elif temperatura > 10:
    print("Jest chłodno.")
else:
    print("Jest zimno.")
```

Program sprawdza temperaturę od najwyższego progu do najniższego. Wykona się tylko pierwszy pasujący komunikat.

## Proste menu wyboru

```python
wybor = int(input("Wybierz opcję: 1 - start, 2 - ustawienia, 3 - koniec: "))

if wybor == 1:
    print("Wybrano start.")
elif wybor == 2:
    print("Wybrano ustawienia.")
elif wybor == 3:
    print("Wybrano koniec.")
else:
    print("Nieznana opcja.")
```

Program sprawdza, którą liczbę wpisał użytkownik. Jeśli wybór to `1`, `2` albo `3`, pojawia się odpowiedni komunikat. Inna liczba trafia do części `else`.

## Klasyfikacja liczby

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba jest dodatnia.")
elif liczba < 0:
    print("Liczba jest ujemna.")
else:
    print("Liczba jest równa zero.")
```

Omówienie wiersz po wierszu:

Pierwszy wiersz wczytuje liczbę całkowitą.

Pierwszy warunek sprawdza, czy liczba jest większa od `0`.

Jeśli pierwszy warunek jest fałszywy, `elif` sprawdza, czy liczba jest mniejsza od `0`.

Jeśli liczba nie jest większa od `0` i nie jest mniejsza od `0`, musi być równa `0`, więc wykonuje się `else`.

## Typowe błędy uczniów

### Kilka oddzielnych if zamiast if-elif-else

Gdy trzeba wybrać jedną z kilku możliwości, często lepsze jest `if-elif-else` niż kilka osobnych instrukcji `if`.

```python
punkty = int(input("Podaj liczbę punktów: "))

if punkty >= 90:
    print("Ocena bardzo dobra")
if punkty >= 75:
    print("Ocena dobra")
if punkty >= 50:
    print("Ocena dostateczna")
```

W takim kodzie może wykonać się kilka części. W konstrukcji `if-elif-else` wykona się tylko jedna część.

### Brak dwukropka po elif

```python
punkty = int(input("Podaj liczbę punktów: "))

if punkty >= 90:
    print("Ocena bardzo dobra")
elif punkty >= 75
    print("Ocena dobra")
```

Po `elif` musi być dwukropek `:`.

### Dopisanie warunku po else

```python
liczba = int(input("Podaj liczbę: "))

if liczba > 0:
    print("Liczba dodatnia")
else liczba == 0:
    print("Zero")
```

`else` nie ma własnego warunku. Jeśli chcesz sprawdzić kolejny warunek, użyj `elif`.

### Zła kolejność warunków

```python
punkty = 95

if punkty >= 50:
    print("Dostateczny")
elif punkty >= 90:
    print("Bardzo dobry")
```

Dla `95` punktów program wypisze `"Dostateczny"`, bo pierwszy warunek jest już prawdziwy i Python nie sprawdzi kolejnego `elif`.

Najpierw zapisujemy warunki bardziej szczegółowe albo wyższe progi.

### Brak wcięć

```python
punkty = int(input("Podaj liczbę punktów: "))

if punkty >= 90:
print("Ocena bardzo dobra")
elif punkty >= 75:
print("Ocena dobra")
else:
print("Brak zaliczenia")
```

Instrukcje należące do `if`, `elif` i `else` muszą być wcięte.

### Mylenie = oraz ==

```python
wybor = int(input("Wybierz opcję: "))

if wybor = 1:
    print("Start")
```

Znak `=` służy do przypisania wartości. Do porównania używamy `==`.

### Myślenie, że może wykonać się kilka części naraz

W konstrukcji `if-elif-else` wykona się tylko jedna część. Python sprawdza warunki od góry do dołu i zatrzymuje się przy pierwszym spełnionym warunku.

## Ćwiczenia

1. Wczytaj liczbę i sprawdź, czy jest dodatnia, ujemna, czy równa zero.
2. Wczytaj liczbę punktów i wypisz ocenę według prostych progów.
3. Wczytaj temperaturę i wypisz komunikat: gorąco, ciepło, chłodno albo zimno.
4. Wczytaj numer dnia tygodnia od 1 do 7 i wypisz nazwę dnia.
5. Wczytaj numer miesiąca od 1 do 12 i wypisz nazwę miesiąca.
6. Wczytaj wiek i wypisz kategorię: dziecko, nastolatek, osoba dorosła.
7. Wczytaj liczbę i sprawdź, czy jest mniejsza od 10, równa 10, czy większa od 10.
8. Wczytaj wybór użytkownika: 1 - nowa gra, 2 - ustawienia, 3 - wyjście.
9. Wczytaj średnią ocen i wypisz krótki komunikat opisowy.
10. Wczytaj prędkość pojazdu i wypisz komunikat: wolno, normalnie, szybko.

## Sposób oddania pracy

Uczeń zapisuje rozwiązania ćwiczeń w swoim folderze w JupyterLab.
