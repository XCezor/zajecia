# Polecenie NL w systemie Linux

Za pomocą polecenia **nl** możemy wyświetlić zawartość pliku wraz z ponumerowanymi wierszami.

## Składnia polecenia wygląda następująco: 
> nl [OPCJE] [Nazwa_Pliku] 

Jeśli podczas wywołania polecenia nie podamy nazwy pliku, to program będzie czytać dane ze standardowego wejścia (czyt. klawiatura).
Aby określić, które linie mają być numerowane musimy użyć opcji -b, która dodatkowo przyjmuje argument w postaci stylu numeracji

Stylem może być:
- a - Wszystkie linie
- t - Tylko nie puste
- n - Brak numeracji

Jeśli z jakiś powodów potrzeba by było numerować linie, lecz licznik miałby zostać inkrementowany o inną liczbę, niż standardowo 1, możemy użyć do tego celu opcji **-i**.
Przykład
>nl -i 10 [Nazwa_Pliku]

Polecenie umożliwia zmianę formatu numeracji za pomocą opcji **-n / --number-format=FORMAT**
Do dyspozycji mamy 3 formaty
  - ln - Wyrównany do lewej krawędzi, bez wiodących zer
  - rn - Wyrównany do prawej krawędzi, bez wiodących zer
  - rz - Wyrównany do prawej krawędzi, z wiodącymi zerami

  Standardowym separatorem pomiędzy numeracją, a tekstem jest tabulacja. Jeśli chcemy to zmienić, to możemy to zrobić z użyciem opcji **-s / --number-separator=STRING**
