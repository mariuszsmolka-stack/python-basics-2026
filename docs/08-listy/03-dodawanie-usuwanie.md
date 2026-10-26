---
layout: default
title: Dodawanie i usuwanie elementów
---

# Dodawanie i usuwanie elementów

## Cel lekcji

Nauczysz się zmieniać liczbę elementów listy. Wybierzesz sposób dodawania lub usuwania zależnie od tego, czy znasz pozycję, czy wartość.

## Czego się nauczysz

- Dodawać na końcu przez `append()`.
- Wstawiać na wskazanej pozycji przez `insert()`.
- Usuwać i odbierać element przez `pop()`.
- Usuwać pierwsze wystąpienie wartości przez `remove()`.

## Co oznacza kropka przy nazwie listy?

**Metoda** to polecenie związane z daną wartością, tutaj z listą. W zapisie `oceny.append(5)` najpierw wskazujemy listę, potem po kropce metodę. W nawiasach podajemy potrzebną daną, czyli argument.

Nie definiujemy własnej funkcji. Korzystamy z operacji, które lista już udostępnia.

## Pierwszy przykład: append()

`append()` dopisuje jeden element na końcu. Nie zastępuje istniejącej wartości.

```python
oceny = [3, 4]
oceny.append(5)
print(oceny)
print(len(oceny))
```

Wynik:

```text
[3, 4, 5]
3
```

## Omówienie działania programu

1. Lista początkowo zawiera dwie oceny.
2. `oceny.append(5)` dopisuje trzeci element.
3. Pierwsze dwie oceny pozostają bez zmian.
4. Długość rośnie z `2` do `3`.

Aby dopisać dwie wartości, wywołaj metodę dwa razy. W tej lekcji dodajemy pojedyncze liczby lub napisy. Dopisanie listy przez `append()` wstawiłoby całą tę listę jako jeden element, a nie jej osobne wartości.

## Wstawianie przez insert()

`insert(indeks, wartość)` wstawia wartość przed elementem z podanej pozycji. Dotychczasowe elementy od tego miejsca przesuwają się w prawo.

```python
imiona = ["Ala", "Maja"]
imiona.insert(1, "Olek")
print(imiona)
imiona.insert(0, "Ewa")
print(imiona)
```

Wynik:

```text
['Ala', 'Olek', 'Maja']
['Ewa', 'Ala', 'Olek', 'Maja']
```

Pierwsze wywołanie wstawia nową osobę przed Mają. Drugie wstawia Ewę na początku. `insert(len(lista), wartość)` wstawia na końcu. W odróżnieniu od odczytu przez indeks, `insert()` dopuszcza też indeks poza zakresem: zbyt duży oznacza koniec, a bardzo mały początek. Na razie wybieraj pozycje od `0` do `len(lista)`.

## Usuwanie przez pop()

`pop()` bez argumentu usuwa ostatni element i **zwraca** jego wartość. Zwracanie oznacza, że możemy ten wynik zapisać w zmiennej. `pop(indeks)` usuwa element ze wskazanej pozycji.

```python
punkty = [10, 20, 30]
usunietePunkty = punkty.pop()
print(usunietePunkty)
print(punkty)
pierwszyWynik = punkty.pop(0)
print(pierwszyWynik)
print(punkty)
```

Wynik:

```text
30
[10, 20]
10
[20]
```

Najpierw usuwamy i zapamiętujemy `30`. Później usuwamy `10` z pozycji `0`. Pozostałe elementy przesuwają się, więc po usunięciu trzeba na nowo ustalić ich indeksy.

## Usuwanie przez remove()

`remove(wartość)` szuka wartości i usuwa jej **pierwsze** wystąpienie. Argument nie jest indeksem.

```python
oceny = [4, 3, 4, 5]
oceny.remove(4)
print(oceny)
```

Wynik:

```text
[3, 4, 5]
```

Druga czwórka zostaje. Gdybyśmy użyli `pop(4)`, próbowalibyśmy usunąć element z piątej pozycji, której ta lista nie ma.

| Operacja | Co podajesz? | Co się zmienia? |
| --- | --- | --- |
| `append(wartość)` | jedną wartość | nowy element na końcu |
| `insert(indeks, wartość)` | pozycję i wartość | nowy element przed wskazaną pozycją |
| `pop(indeks)` | pozycję | usunięcie elementu i zwrócenie go |
| `pop()` | nic | usunięcie i zwrócenie ostatniego |
| `remove(wartość)` | wartość | usunięcie pierwszego wystąpienia |

## Typowe błędy

Nie można odczytać nieistniejącego indeksu ani usunąć go przez `pop()`. Takie działanie powoduje `IndexError`. `pop()` na pustej liście również powoduje `IndexError`.

Jeśli wartości przekazanej do `remove()` nie ma w liście, program kończy się błędem `ValueError`. To błąd związany z niewłaściwą wartością argumentu. Poniższy kompletny przykład celowo kończy się błędem:

```python
oceny = [3, 4]
oceny.remove(6)
```

Ostatnia linia komunikatu błędu:

```text
ValueError: list.remove(x): x not in list
```

Nie zakładaj, że `remove()` cicho zignoruje brak wartości. Sprawdzanie jej obecności poznasz w lekcji 05.

Nie myl `append()` ze zmianą elementu przez indeks. Dodanie zwiększa długość, a zastąpienie wartości na istniejącej pozycji jej nie zmienia.

## Ćwiczenia

### Ćwiczenie 1. Jeszcze jedna ocena

Do listy `oceny = [3, 4]` dopisz `6`. Wypisz listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 1</summary>

Chodzi o nowy element na końcu. Nie zastępuj żadnej z dwóch dotychczasowych ocen.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 1</summary>

```python
oceny = [3, 4]
oceny.append(6)
print(oceny)
```

Wynik:

```text
[3, 4, 6]
```

</details>

### Ćwiczenie 2. Osoba na początku

Do listy `kolejka = ["Ala", "Olek"]` wstaw `"Ewa"` na początku. Wypisz listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 2</summary>

Pierwsza pozycja ma indeks zero. Dotychczasowe osoby mają pozostać w kolejce.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 2</summary>

```python
kolejka = ["Ala", "Olek"]
kolejka.insert(0, "Ewa")
print(kolejka)
```

Wynik:

```text
['Ewa', 'Ala', 'Olek']
```

</details>

### Ćwiczenie 3. Ostatni wynik

Z listy `wyniki = [12, 15, 9]` usuń ostatni element. Wypisz usuniętą wartość i pozostałą listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 3</summary>

Potrzebujesz operacji, która oprócz usunięcia oddaje usuwaną wartość.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 3</summary>

```python
wyniki = [12, 15, 9]
usunietyWynik = wyniki.pop()
print(usunietyWynik)
print(wyniki)
```

Wynik:

```text
9
[12, 15]
```

</details>

### Ćwiczenie 4. Usuwanie według wartości

Z listy `liczby = [2, 8, 2, 5]` usuń tylko pierwszą dwójkę. Wypisz listę.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 4</summary>

Znasz wartość do usunięcia. Druga taka sama wartość ma zostać.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 4</summary>

```python
liczby = [2, 8, 2, 5]
liczby.remove(2)
print(liczby)
```

Wynik:

```text
[8, 2, 5]
```

</details>

### Ćwiczenie 5. Zmiana planu

Zacznij od `plan = ["lekcje", "trening", "film"]`. Usuń element z indeksem `1`. Na tej samej pozycji wstaw `"spacer"`. Wypisz plan.

<details markdown="1">
<summary>Podpowiedź do ćwiczenia 5</summary>

Najpierw usuń wskazaną pozycję. Po usunięciu film przesunie się w lewo. Nową czynność wstaw przed nim.

</details>

<details markdown="1">
<summary>Rozwiązanie ćwiczenia 5</summary>

```python
plan = ["lekcje", "trening", "film"]
plan.pop(1)
plan.insert(1, "spacer")
print(plan)
```

Wynik:

```text
['lekcje', 'spacer', 'film']
```

</details>

## Podsumowanie

Wybieraj metodę według celu. `append()` i `insert()` dodają element. `pop()` usuwa pozycję i oddaje wartość. `remove()` usuwa pierwsze wystąpienie podanej wartości.
