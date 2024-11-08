# Komenda `sed` modyfikuje wiersze z określonego parametru `Plik` zgodnie ze skryptem edycji i zapisuje je na wyjściu standardowym. Zawiera funkcje wybierające wiersze do modyfikacji i wprowadzania zmian tylko do wybranych wierszy.

## Składnia:
```sh
sed [ -n ] [ -u ] Skrypt  [ Plik ... ]

sed [ -n ] [ -u ] [ -e Skrypt ] ... [ -f ScriptFile ] ... [ Plik ... ]
```
\
\
Komenda sed używa dwóch obszarów roboczych do przechowywania modyfikowanego wiersza: **obszaru wzorca**, w którym znajduje się wybrana linia, oraz **obszaru wstrzymania**, w którym wiersz może być tymczasowo przechowywany.
\
\
Skrypt edycji składa się z poszczególnych podkomend, a każdy z nich znajduje się w osobnym wierszu. Ogólna postać podkomend produktu sed jest następująca:

```sh
[zakres adresów] funkcja[modyfikatory]
```

## Można zatem powiedzieć, że komenda `sed` podmienia dany fragment pliku na inny
## Przykład:
```sh
sed 's/Sed/Des' sed_test.txt
```
Komenda ta wyświetli zawartość pliku sed_test.txt i tylko do podlądu zamieni wszystkie napisy `Sed` na `Des`. Wynik tej komendy można sprawdzić w pliku `sed przykład.png`.

## Jeżeli chcemy zapisać zmiany wprowadzone komendą `sed`, na końcu polecenia można dodać `>nazwa_pliku.txt`
## Przykład:
```sh
sed 's/Sed/Des' sed_test.txt >sed_test_dwa.txt
```
Polecenie utworzy nowy plik `sed_test_dwa.txt` w tym samym katalogu, z podmienionymi napisami `Sed` na `Des`. Wynik można zobaczyć na zdjęciu `sed kopiowanie pliku.png`.