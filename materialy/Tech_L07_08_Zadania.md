# Karta Zadań: Analiza danych w arkuszu kalkulacyjnym

***

## CZĘŚĆ 1: Przykłady

**Przykład 1: Użycie formuły IF w logach**
Problem: Kolumna B zawiera status HTTP żądania (np. 200, 404, 500). W kolumnie C chcemy oznaczyć, czy żądanie to "SUKCES" (status < 400) czy "BŁĄD" (status >= 400).
Rozwiązanie formuły dla drugiego wiersza:
`=IF(B2 < 400; "SUKCES"; "BŁĄD")`

**Przykład 2: Zliczanie specyficznych błędów**
Problem: Chcemy policzyć, ile wierszy w kolumnie D (Kody Błędów od D2 do D500) zawiera kod błędu 500.
Rozwiązanie:
`=COUNTIF(D2:D500; 500)`

***

## CZĘŚĆ 2: Zadania do wykonania

**Zadanie 1: Oczyszczanie danych**
Otrzymałeś plik z adresami e-mail użytkowników, ale na skutek błędu systemu, na początku niektórych adresów pojawiły się spacje (np. "  jan.kowalski@it.pl"). Napisz, jakiej formuły z rodziny operacji tekstowych użyjesz w komórce B2, aby oczyścić komórkę A2.

Twoja odpowiedź: ______________________________________________________________

**Zadanie 2: Formuła do zliczania**
Posiadasz rejestr incydentów bezpieczeństwa. W kolumnie A są opisane zdarzenia (od A2 do A1000), a w kolumnie C jest zapisany priorytet ("Niski", "Średni", "Wysoki", "Krytyczny").
Napisz formułę, która policzy, ile incydentów ma priorytet "Krytyczny".

Twoja odpowiedź: ______________________________________________________________

**Zadanie 3: Scenariusz z VLOOKUP**
Masz dwa arkusze. W Arkuszu1 w kolumnie A masz numery ID pracowników. W Arkuszu2 w pierwszej kolumnie masz numery ID, a w drugiej Nazwiska.
Napisz, jak mniej więcej wyglądałaby formuła z wykorzystaniem VLOOKUP (WYSZUKAJ.PIONOWO), aby w Arkuszu1 przy ID pracownika wyświetliło się jego nazwisko.

Twoja odpowiedź: 
______________________________________________________________________________
______________________________________________________________________________

**Zadanie 4: Zastosowanie Tabeli Przestawnej**
Masz logi zawierające 5000 wierszy. Każdy wiersz to log odwiedzin strony. Kolumna A to Data, Kolumna B to Adres IP, Kolumna C to Przeglądarka (Chrome, Firefox, itp.).
Opisz krótko (w 2-3 krokach), co ustawisz w Tabeli Przestawnej (Wiersze, Wartości), aby dowiedzieć się, z jakiej przeglądarki korzystano najczęściej.

Twoja odpowiedź: 
______________________________________________________________________________
______________________________________________________________________________
______________________________________________________________________________
