# JupyterLab

JupyterLab to środowisko, w którym możemy pisać i uruchamiać kod Pythona. Jest wygodne na początku nauki, bo szybko pokazuje wynik działania programu.

## Notatnik

W JupyterLab często pracujemy w notatniku. Taki plik ma rozszerzenie `.ipynb`.

Notatnik składa się z komórek. Każdą komórkę można uruchomić osobno.

## Komórka kodu i komórka Markdown

Komórka kodu służy do pisania programu w Pythonie.

Komórka Markdown służy do notatek, opisów i krótkich wyjaśnień. Nie wpisujemy w niej kodu, który ma zostać wykonany przez Pythona.

## Tworzenie nowego notatnika

Aby rozpocząć pracę, utwórz nowy notatnik Python. Zapisz go w swoim folderze i nadaj mu czytelną nazwę, na przykład:

```text
lekcja_01_pierwszy_program.ipynb
```

## Wpisywanie i uruchamianie kodu

Kod wpisujemy w komórce kodu. Aby uruchomić komórkę, można użyć skrótu:

```text
Shift+Enter
```

Przykład:

```python
imie = "Anna"
print("Witaj", imie)
```

Po uruchomieniu komórki JupyterLab pokaże wynik pod kodem.

## Kolejność wykonywania komórek

Kolejność uruchamiania komórek ma znaczenie. Jeśli zmienna została utworzona w jednej komórce, a potem użyta w drugiej, najpierw trzeba uruchomić komórkę ze zmienną.

Jeżeli wynik programu wygląda dziwnie, warto uruchomić notatnik od początku.

## Kernel

Kernel to część JupyterLab, która wykonuje kod Pythona. Czasem warto go ponownie uruchomić, aby zacząć pracę od czystego stanu.

Po ponownym uruchomieniu kernela trzeba uruchomić komórki jeszcze raz, od początku.

## Uruchomienie wszystkich komórek

W JupyterLab można uruchomić wszystkie komórki od początku. To dobry sposób, aby sprawdzić, czy cały notatnik działa poprawnie.

## Pliki `.ipynb` i `.py`

Plik `.ipynb` to notatnik JupyterLab. Może zawierać kod, wyniki i notatki.

Plik `.py` to zwykły plik z programem w Pythonie. W projektach końcowych często zapisujemy ostateczną wersję programu właśnie jako plik `.py`.

## Bezpieczna praca z plikami

- Zapisuj pliki w swoim folderze.
- Nadawaj plikom czytelne nazwy.
- Nie usuwaj cudzych plików.
- Regularnie zapisuj swoją pracę.
- Przed oddaniem uruchom program jeszcze raz i sprawdź wynik.
