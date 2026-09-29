# ⚡ KARTA ZADAŃ ZAAWANSOWANYCH: Architektura Prywatności & Sieci (Technikum)
## Pakiet Audytorski do Google Classroom: Topologia Tor, DNS Sinkhole & Izolacja Systemowa
**Autor:** Przemysław Żarnecki • Program Edukacyjny INFOTECH 2026  
**Poziom:** Rozszerzony / Zawodowy (Technikum Informatyczne) • **Rola:** Inżynier Bezpieczeństwa (Blue Team)

---

## 🎯 CELE OPERACYJNE ZADANIA
Po zrealizowaniu zadań uczeń:
* Rozumie topologię trasowania cebulowego (Onion Routing) oraz zagrożenia związane z podsłuchem na węźle wyjściowym (Tor Exit Node Sniffing).
* Potrafi zaprojektować politykę filtrowania ruchu sieciowego na poziomie serwera DNS (technologia DNS Sinkhole / Pi-Hole).
* Rozumie koncepcję *Security by Isolation* w systemach hiperwizora (np. Qubes OS / wirtualizacja kontenerowa).

---

## 💡 CZĘŚĆ 1: Studium Przypadku (Wzorcowa Analiza Inżynierska)

### Scenariusz Badawczy: Nieszyfrowany protokół HTTP w sieci Tor
* **Sytuacja:** Użytkownik przegląda podejrzane strony z użyciem przeglądarki Tor Browser. Wchodzi na witrynę, która nie posiada certyfikatu SSL (protokół `http://` zamiast `https://`).
* **Problem:** Ruch wewnątrz sieci Tor jest trzykrotnie szyfrowany między węzłem wejściowym (Guard Node) a węzłem pośrednim (Middle Node). W którym jednak miejscu dane stają się jawne dla hakera nasłuchującego sieć?
* **Wzorcowa odpowiedź inżyniera:**  
  *„Dane stają się jawne na wyjściu z **Węzła Wyjściowego (Exit Node)**. Exit Node jako ostatni element łańcucha zdejmuje ostatnią warstwę szyfrowania cebulowego i przesyła pakiet otwartym tekstem przez publiczny Internet do serwera docelowego. Jeśli strona nie stosuje HTTPS, operator złośliwego Exit Node'a (np. wywiad lub cyberprzestępca) widzi wszystkie loginy, hasła i nieszyfrowane zapytania użytkownika. Sieć Tor ukrywa adres IP nadawcy, ale **nie chroni treści pakietów HTTP przed złośliwym węzłem wyjściowym**!”*

---

## 📋 CZĘŚĆ 2: ZADANIA AUDYTORSKIE DLA CIEBIE (DO ODDANIA W CLASSROOM)

Rozwiąż poniższe 3 problemy z perspektywy inżyniera bezpieczeństwa IT (Blue Team).

### 🔒 Zadanie 1: Kwestia Zaufania w Tunelach VPN (Threat Modeling)
* **Sytuacja:** Młodszy administrator zainstalował na smartfonach firmowych darmową aplikację VPN pobraną z niezweryfikowanego repozytorium zewnętrznego, argumentując to: *„Przynajmniej operator komórkowy Play/Orange nie podgląda naszego ruchu”*.
* **Polecenie:** Sporządź profesjonalną notatkę audytorską. Używając pojęcia *tunelowania* i *wektora ataku Man-in-the-Middle (MitM)*, wyjaśnij, dlaczego niezweryfikowany darmowy VPN stanowi znacznie większe zagrożenie dla firmy niż bezpośrednie połączenie przez oficjalnego dostawcę internetu (ISP). Kto w tym momencie ma wgląd w całą historię zapytań DNS i niezaszyfrowany ruch?

### 🛡️ Zadanie 2: Architektura DNS Sinkhole (Pi-Hole) vs Wtyczki Przeglądarki
* **Sytuacja:** W pracowni szkolnej komputery oraz smartfony podłączone do Wi-Fi masowo pobierają złośliwe reklamy (Malvertising) oraz trackery w aplikacjach mobilnych. Zamiast instalować wtyczki uBlock Origin na 120 urządzeniach, proponujesz wdrożenie serwera **Pi-Hole (DNS Sinkhole)** na poziomie bramy sieciowej.
* **Polecenie:** Wyjaśnij mechanizm działania DNS Sinkhole. Co dzieje się z zapytaniem o domenę śledzącą (np. `adservice.google.com` lub domenę z malware), gdy urządzenie odpytuje lokalny serwer DNS? Dlaczego rozwiązanie to blokuje reklamy także w aplikacjach mobilnych (np. w grach na telefonie), w których nie da się zainstalować wtyczki do przeglądarki?

### 📦 Zadanie 3: Zasada Izolacji Systemowej (Architektura Qubes OS)
* **Sytuacja:** Pracujesz w dziale Cyber Threat Intelligence w banku. Codziennie analizujesz potencjalnie złośliwe pliki PDF i wykonywalne `.exe` nadesłane w wiadomościach phishingowych.
* **Polecenie:** Wyjaśnij zasadę *Security through Isolation* w systemie **Qubes OS** (opartym na mikrojądrze i hiperwizorze Xen). Co stanie się, jeśli analityk uruchomi złośliwy plik w wirtualnej maszynie typu Disposable VM (jednorazowa kostka)? Dlaczego malware nie jest w stanie zainfekować systemu bazowego ani wykraść certyfikatów bankowych uruchomionych w innej kostce (Vault)?

---

## 📊 KRYTERIA OCENY (NaCoBeZu):
* **Dostateczny (3):** Ogólna odpowiedź na Zadanie 1 i 2 bez użycia terminologii sieciowej.
* **Dobry (4):** Poprawna analiza tunelowania VPN (Zadanie 1) oraz zasady odpowiedzi DNS 0.0.0.0 w Pi-Hole (Zadanie 2).
* **Bardzo Dobry (5):** Kompletna, profesjonalna analiza techniczna wszystkich 3 zadań z użyciem pojęć: *Exit Node, MitM, DNS Sinkhole, Hiperwizor Type-1, Disposable VM*.
* **Celujący (6) - Wyzwanie:** Zaprojektowanie reguły iptables lub schematu konfiguracji pliku `hosts` przekierowującego zapytania reklamowe na adres pętli zwrotnej `0.0.0.0` (Localhost)!

---

## ✍️ FORMULARZ ODPOWIEDZI UCZNIA (Wklej do Google Classroom):
```text
--- FORMULARZ AUDYTORSKI: ARCHITEKTURA PRYWATNOŚCI (Technikum) ---
Imię i Nazwisko: [TWOJE IMIĘ I NAZWISKO]
Klasa / Profil: [NP. 2TI TECHNIKUM]
Data: [RRRR-MM-DD]

ZADANIE 1: ANALIZA RYZYKA DARMOWEGO TUNELU VPN:
- Co technicznie dzieje się z ruchem sieciowym po włączeniu VPN?:
  [Odpowiedź: Cały ruch zostaje przekierowany przez serwer dostawcy VPN...]
- Dlaczego darmowy, niesprawdzony VPN jest groźniejszy niż lokalny ISP?:
  [Uzasadnienie: Dostawca darmowego VPN może logować zapytania, wstrzykiwać reklamy i prowadzić atak MitM...]

ZADANIE 2: MECHANIZM DNS SINKHOLE (PI-HOLE):
- W jaki sposób Pi-Hole blokuje zapytania o domeny reklamowe?:
  [Odpowiedź: Zwraca adres 0.0.0.0 zamiast prawdziwego IP serwera reklamy...]
- Dlaczego to rozwiązanie działa również na smartfonach i Smart TV?:
  [Uzasadnienie: Blokada następuje na poziomie rezolucji nazw DNS dla całej sieci LAN...]

ZADANIE 3: ARCHITEKTURA IZOLACJI (QUBES OS / XEN):
- Co dzieje się ze złośliwym oprogramowaniem po uruchomieniu w Disposable VM?:
  [Odpowiedź: Zostaje uwięziony w odizolowanym kontenerze Xen i znika po wyłączeniu kostki...]
- Dlaczego wirus nie ma dostępu do danych w kostce 'Vault'?:
  [Uzasadnienie: Hiperwizor uniemożliwia współdzielenie pamięci RAM i przestrzeni dyskowej...]

WYZWANIE NA OCENĘ 6 (OPCJONALNIE):
- [Przykładowa reguła lub wpis w pliku hosts / Pi-Hole]: ...
-----------------------------------------------------------------
```
