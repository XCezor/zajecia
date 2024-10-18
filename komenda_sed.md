# Komenda sed modyfikuje wiersze z określonego parametru Plik zgodnie ze skryptem edycji i zapisuje je na wyjściu standardowym. Zawiera funkcje wybierające wiersze do modyfikacji i wprowadzania zmian tylko do wybranych wierszy.

## Składnia:
```sh
sed [ -n ] [ -u ] Skrypt  [ Plik ... ]

sed [ -n ] [ -u ] [ -e Skrypt ] ... [ -f ScriptFile ] ... [ Plik ... ]
```
\
\
Komenda sed używa dwóch obszarów roboczych do przechowywania modyfikowanego wiersza: **obszaru wzorca**, w którym znajduje się wybrana linia, oraz **obszaru wstrzymania**, w którym wiersz może być tymczasowo przechowywany.
\\
Skrypt edycji składa się z poszczególnych podkomend, a każdy z nich znajduje się w osobnym wierszu. Ogólna postać podkomend produktu sed jest następująca:

```sh
[zakres adresów] funkcja[modyfikatory]
```