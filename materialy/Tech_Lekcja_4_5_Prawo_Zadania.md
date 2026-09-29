# ⚡ KARTA ZADAŃ PROJEKTOWYCH: Audyt Prawny w IT & License Laundering (Technikum)
## Pakiet Dydaktyczny do Google Classroom: Zgodność Licencyjna (Open Source Compliance) i Ryzyko Kodu AI
**Autor:** Przemysław Żarnecki • Program Edukacyjny INFOTECH 2026  
**Poziom:** Rozszerzony / Zawodowy (Technikum Informatyczne) • **Rola:** Lead Developer / Audytor Kodu

---

## 🎯 CELE OPERACYJNE ZADANIA
Po wykonaniu zadań uczeń:
* Rozumie architektoniczne i biznesowe konsekwencje włączenia kodu na licencji GNU GPL do zamkniętych systemów komercyjnych (zasada Copyleft).
* Zna zjawisko *License Laundering* (pranie licencji przez modele LLM) i potrafi zidentyfikować ryzyko prawne w łańcuchu dostaw oprogramowania (Software Supply Chain).
* Rozumie pojęcie SBOM (Software Bill of Materials) i potrafi zaplanować audyt licencyjny zależności projektowych.

---

## 💡 CZĘŚĆ 1: Studium Przypadku (Wzorcowa Analiza Inżynierska)

### Przykład A: Audyt Zależności z Licencją MIT
* **Sytuacja:** Przed wydaniem komercyjnej wersji systemu płatności skaner audytowy (np. `license-checker` w npm) wykazał, że zespół użył 15 bibliotek na licencji **MIT**.
* **Pytanie:** Czy projekt jest zagrożony prawnie i czy firma będzie musiała opublikować swój kod źródłowy?
* **Wzorcowa odpowiedź inżyniera:**  
  *„Nie, licencja MIT to licencja z grupy 'permissive'. Pozwala na łączenie kodu open source z zamkniętym kodem komercyjnym i nie wymaga otwierania źródeł (brak klauzuli copyleft). Jedynym wymogiem audytorskim jest wygenerowanie pliku `THIRD_PARTY_LICENSES.txt` w instalatorze/repozytorium i załączenie w nim oryginalnych not o prawach autorskich twórców tych 15 bibliotek.”*

### Przykład B: Ochrona Prawnoautorska Wytworów LLM
* **Sytuacja:** Zespół użył asystenta AI do wygenerowania 100% specyfikacji i kodu mikroserwisu, a konkurencja skopiowała ten kod wprost ze strony.
* **Pytanie:** Z jakim problemem formalnym spotka się firma w sądzie, próbując pozwać konkurencję o naruszenie autorskich praw majątkowych?
* **Wzorcowa odpowiedź inżyniera:**  
  *„Zgodnie z orzecznictwem w Unii Europejskiej oraz w USA (decyzje US Copyright Office), utwór musi być rezultatem twórczej pracy człowieka. Wytwór wygenerowany w całości przez prompt maszynowy nie podlega ochronie prawa autorskiego – znajduje się w domenie publicznej. Firma nie wykaże w sądzie więzi twórczej między człowiekiem a kodem, przez co powództwo o naruszenie praw autorskich zostanie oddalone.”*

---

## 📋 CZĘŚĆ 2: ZADANIA DLA CIEBIE (DO ODDANIA W GOOGLE CLASSROOM)

Wciel się w rolę Głównego Architekta Oprogramowania (Lead Engineera) i rozwiąż dwa poniższe problemy.

### 🛑 Zadanie 1: Wirus Copyleft w Kodzie Serwera Produkcyjnego
* **Sytuacja:** Tworzycie potężny system bankowości w Node.js, który firma zamierza sprzedawać za miliony złotych instytucjom finansowym. Tuż przed premierą audyt wykazał, że jeden z programistów wkleił do rdzenia systemu bibliotekę na licencji **GNU GPL v3**. Biblioteka jest statycznie powiązana z logiką biznesową.
* **Polecenie:**
  1. Jakie skutki prawne dla całego projektu ma zlekceważenie tej licencji, jeśli aplikacja zostanie wydana komercyjnie?
  2. Wyjaśnij mechanizm działania wirusowej natury (Copyleft) licencji GPL v3 w zamkniętych projektach.
  3. Jakie 2 rozwiązania inżynierskie ma teraz zespół (jak naprawić sytuację przed premierą)?

### 🤖 Zadanie 2: Zjawisko „License Laundering” przez Modele AI
* **Sytuacja:** Używasz asystenta GitHub Copilot. Poprosiłeś o zaawansowany algorytm kompresji danych w czasie rzeczywistym. AI wygenerowało idealny kod. Trzy miesiące później firma otrzymuje pismo od kancelarii prawnej innej korporacji z dowodem, że kod ten został w całości skradziony z ich zastrzeżonego, zamkniętego projektu komercyjnego, na którym model AI trenował (tzw. halucynacja pamięciowa / verbatim extraction).
* **Polecenie:**
  1. Czy przed sądem obroni Was argument: *„To nie nasza wina, kod wygenerowała sztuczna inteligencja”*? Kto w świetle prawa ponosi odpowiedzialność za kod wdrożony na produkcję?
  2. Dlaczego bezkrytyczne kopiowanie kodu z LLM do projektów firmowych stanowi poważne zagrożenie dla łańcucha dostaw oprogramowania (Software Supply Chain)?

---

## 📊 KRYTERIA OCENY (NaCoBeZu):
* **Dostateczny (3):** Podstawowe wyjaśnienie problemu GPL w zadaniu 1 bez rozwiązań inżynierskich.
* **Dobry (4):** Poprawne rozwiązanie Zadania 1 (wyjaśnienie copyleft + 2 drogi naprawy: refaktoryzacja/dual licensing) + ogólna odpowiedź na Zadanie 2.
* **Bardzo Dobry (5):** Ocena 4 + profesjonalna analiza odpowiedzialności prawnej inżyniera za kod z AI oraz mechanizmu *License Laundering*.
* **Celujący (6) - Wyzwanie:** Zaproponowanie procedury **SBOM (Software Bill of Materials)** i narzędzi automatycznego audytu CI/CD (np. Trivy, Syft, FOSSA) wykrywających luki licencyjne przed mergem na gałąź produkcyjną!

---

## ✍️ FORMULARZ ODPOWIEDZI UCZNIA (Wklej do Google Classroom):
```text
--- FORMULARZ AUDYTORSKI: PRAWO W IT & LICENSE COMPLIANCE (Technikum) ---
Imię i Nazwisko: [TWOJE IMIĘ I NAZWISKO]
Klasa / Profil: [NP. 2TI TECHNIKUM]
Data: [RRRR-MM-DD]

ZADANIE 1: WIRUSOWOŚĆ GPL V3 W KODZIE SERWERA:
- Jakie skutki prawne niesie użycie GPL v3 w zamkniętym projekcie?:
  [Odpowiedź: Wymusza udostępnienie całego kodu źródłowego na licencji GPL v3...]
- Jakie 2 opcje inżynierskie ma zespół przed premierą?:
  1) [Usunięcie modułu i napisanie własnej implementacji / zastąpienie biblioteką MIT...]
  2) [Kontakt z autorem i wykupienie licencji komercyjnej (tzw. Dual-Licensing)...]

ZADANIE 2: LICENSE LAUNDERING I ODPOWIEDZIALNOŚĆ ZA KOD AI:
- Czy argument "to wina AI" ma moc prawną w sądzie?:
  [Uzasadnienie: Nie, to programista i firma wdrażająca kod ponoszą 100% odpowiedzialności prawnej...]
- Dlaczego bezkrytyczne wklejanie kodu z LLM jest niebezpieczne w firmie?:
  [Uzasadnienie: Może naruszać patenty, licencje copyleft oraz wprowadzać podatności zero-day...]

WYZWANIE NA OCENĘ 6 (OPCJONALNIE):
- Czym jest SBOM (Software Bill of Materials) i jak automatyzujemy audyt w CI/CD?:
  [Odpowiedź...]
------------------------------------------------------------------------
```
