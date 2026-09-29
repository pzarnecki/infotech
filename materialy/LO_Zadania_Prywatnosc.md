# 🕵️ KARTA ZADAŃ: Prywatność w Sieci & Ślad Cyfrowy (Liceum)
## Pakiet Dydaktyczny do Google Classroom: Narzędzia Prywatności, VPN i Anonimowość
**Autor:** Przemysław Żarnecki • Program Edukacyjny INFOTECH 2026  
**Poziom:** Podstawowy (Liceum Ogólnokształcące) • **Środowisko:** Przeglądarka / System operacyjny

---

## 🎯 CELE OPERACYJNE ZADANIA
Po zrealizowaniu zadań uczeń:
* Rozumie różnicę między lokalną prywatnością (Tryb Incognito) a prywatnością sieciową (VPN, Tor).
* Potrafi wyjaśnić mechanizm profilowania reklamowego za pomocą ciasteczek (*Tracking Cookies*) i cyfrowego odcisku palca (*Browser Fingerprinting*).
* Wie, w jakich sytuacjach korzystanie z publicznych sieci Wi-Fi wymaga tunelowania VPN.

---

## 💡 CZĘŚĆ 1: Przykłady Wzorcowych Rozwiązań (Jak Poprawnie Odpowiadać)

### Przykład A: Publiczne Wi-Fi w Kawiarni
* **Opis sytuacji:** Jesteś w kawiarni i łączysz się z darmowym, otwartym Wi-Fi bez hasła. Chcesz zalogować się do swojego konta bankowego, ale obawiasz się, że ktoś w kawiarni podsłuchuje ruch sieciowy (np. używając programu Wireshark/sniffer).
* **Pytanie:** Jakiego narzędzia użyjesz i dlaczego?
* **Wzorcowa odpowiedź ucznia:**  
  *„Użyję zaufanej usługi **VPN (Virtual Private Network)**. Skoro sieć Wi-Fi jest otwarta i nieszyfrowana, każdy użytkownik w kawiarni mógłby przechwytywać nieszyfrowane pakiety danych. VPN tworzy szyfrowany tunel między moim laptopem a serwerem VPN. Haker nasłuchujący ruch w kawiarni zobaczy jedynie nieczytelny, zaszyfrowany strumień bajtów i nie pozna moich haseł ani przeglądanych stron.”*

### Przykład B: Uporczywy Remarketing Reklamowy
* **Opis sytuacji:** Po przeglądaniu butów sportowych w sklepie internetowym, przez kolejne dwa tygodnie na każdym portalu informacyjnym, pogodowym i w social mediach widzisz reklamy dokładnie tych samych butów.
* **Pytanie:** Jakie zjawisko tu zaszło i jak mu zapobiec?
* **Wzorcowa odpowiedź ucznia:**  
  *„Zaszło zjawisko śledzenia międzywitrynowego za pomocą **zewnętrznych ciasteczek (Third-party Tracking Cookies)** oraz skryptów analitycznych (np. pikseli reklamowych Meta i Google). Aby temu zapobiec, zainstaluję w przeglądarce wtyczkę blokującą skrypty śledzące (np. **uBlock Origin**) oraz włączę w ustawieniach przeglądarki opcję 'Blokuj pliki cookie innych firm'.”*

---

## 📋 CZĘŚĆ 2: ZADANIA DLA CIEBIE (DO ODDANIA W GOOGLE CLASSROOM)

Rozwiąż 3 poniższe case studies, wzorując się na przykładach z Części 1.

### 🏢 Zadanie 1: Komputer w Bibliotece Szkolnej
* **Opis sytuacji:** Jesteś w szkolnej bibliotece i musisz zalogować się na chwilę na swoje prywatne konto e-mail/Discord na ogólnodostępnym komputerze, z którego w ciągu dnia korzysta kilkudziesięciu innych uczniów.
* **Pytanie:** Z jakiego trybu w przeglądarce powinieneś skorzystać przed wejściem na stronę? Co dokładnie dzieje się po zamknięciu okna tego trybu i przed czym Cię to chroni, a przed czym NIE chroni?

### 🌍 Zadanie 2: Omijanie Blokad Geograficznych na Wyjeździe
* **Opis sytuacji:** Wyjechałeś na wakacje za granicę (lub do kraju z cenzurą internetu). Próbujesz obejrzeć polski serwis VOD (np. TVP VOD, Polsat Box lub Netflix), ale strona wyświetla błąd: *„Materiał niedostępny w Twoim regionie geograficznym”*.
* **Pytanie:** Jakiego narzędzia użyjesz, aby serwisy myślały, że nadal łączysz się z terytorium Polski? Wyjaśnij w 2 zdaniach, jak dochodzi do zmiany Twojego publicznego adresu IP.

### 🕶️ Zadanie 3: Skrajna Anonimowość – Dziennikarz Śledczy
* **Opis sytuacji:** Jesteś dziennikarzem i musisz anonimowo przesłać dokumenty obciążające potężną korporację. Wiesz, że zwykły komercyjny VPN może prowadzić logi lub ugiąć się pod nakazem sądowym.
* **Pytanie:** Jakiego darmowego, rozproszonego systemu sieciowego użyjesz (tzw. sieć cebulowa)? Jak działa trasowanie pakietów przez 3 losowe węzły (Guard, Middle, Exit)?

---

## 📊 KRYTERIA OCENY (NaCoBeZu):
* **Dostateczny (3):** Udzielenie odpowiedzi na Zadanie 1 i 2 bez zagłębiania się w szczegóły techniczne.
* **Dobry (4):** Poprawne rozwiązanie Zadań 1, 2 i 3 z wyjaśnieniem pojęć Trybu Incognito, VPN i sieci Tor.
* **Bardzo Dobry (5):** Ocena 4 + precyzyjne rozróżnienie: przed czym tryb incognito chroni (ciasteczka i historia lokalna), a przed czym NIE chroni (dostawca ISP, administrator sieci szkolnej widzą ruch).
* **Celujący (6) - Wyzwanie:** Wskazanie pojęcia *Browser Fingerprinting* (odcisk palca przeglądarki: czcionki, rozdzielczość ekranu, Canvas API) i wyjaśnienie, dlaczego pozwala śledzić użytkownika nawet bez plików cookies!

---

## ✍️ FORMULARZ ODPOWIEDZI UCZNIA (Wklej do Google Classroom):
```text
--- FORMULARZ ODPOWIEDZI: PRYWATNOŚĆ W SIECI (Liceum) ---
Imię i Nazwisko: [TWOJE IMIĘ I NAZWISKO]
Klasa: [NP. 1A LO]
Data: [RRRR-MM-DD]

ZADANIE 1 (KOMPUTER W BIBLIOTECE):
- Tryb przeglądarki, którego użyję: [WPISZ TUTAJ]
- Co dzieje się z moją sesją po zamknięciu tego okna?: [WYJAŚNIENIE...]
- Przed czym ten tryb MNIE NIE CHRONI?: [WYJAŚNIENIE...]

ZADANIE 2 (BLOKADA GEOGRAFICZNA):
- Narzędzie do zmiany lokalizacji IP: [WPISZ TUTAJ]
- W jaki sposób serwer VOD widzi polski adres IP?: [WYJAŚNIENIE...]

ZADANIE 3 (SKRAJNA ANONIMOWOŚĆ):
- Nazwa sieci cebulowej i dedykowanej przeglądarki: [WPISZ TUTAJ]
- Na czym polega wielowarstwowe szyfrowanie przez węzły?: [WYJAŚNIENIE...]

WYZWANIE NA OCENĘ 6 (OPCJONALNIE):
- Czym jest Browser Fingerprinting i jak serwisy rozpoznają nas bez cookies?:
  [WYJAŚNIENIE...]
---------------------------------------------------------
```
