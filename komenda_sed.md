# Komenda sed modyfikuje wiersze z określonego parametru Plik zgodnie ze skryptem edycji i zapisuje je na wyjściu standardowym. Zawiera funkcje wybierające wiersze do modyfikacji i wprowadzania zmian tylko do wybranych wierszy.

## Składnia:
```sed [ -n ] [ -u ] Skrypt  [ Plik ... ]```
\
```sed [ -n ] [ -u ] [ -e Skrypt ] ... [ -f ScriptFile ] ... [ Plik ... ]```