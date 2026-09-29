# ⚡ MODUŁ PROJEKTOWY: KRYPTOGRAFIA & BIAŁY WYWIAD (OSINT)
## Materiały Edukacyjne do Google Classroom: Zblokowane Lekcje 2-3 (Technikum)
**Autor:** Przemysław Żarnecki • Program Edukacyjny INFOTECH 2026  
**Profil:** Technikum Informatyczne / Programistyczne (Ścieżka Zawodowa)  
**Środowisko:** Google Colab (Python 3.10+) / Przeglądarka internetowa / DevTools

---

## 📌 ZAŁOŻENIA METODYCZNE DLA NAUCZYCIELA TECHNIKUM
Uczniowie technikum mają w planie przedmioty zawodowe (kwalifikacje INF.03 i INF.04), na których uczą się składni języków i podstaw algorytmiki. Na zajęciach ogólnych z informatyki **nie dublujemy nudnego pisania prostych pętli**.  
Zamiast tego wchodzimy w **rolę Red Teamu (Audytorów Bezpieczeństwa)**:
* Łączymy skryptowanie w Pythonie z realną architekturą bezpieczeństwa serwerów.
* Tłumaczymy matematyczne i fizyczne ograniczenia sprzętu (GPU vs ASIC vs CPU).
* Analizujemy realne incydenty bezpieczeństwa w polskich przedsiębiorstwach.

---

# 🧠 CZĘŚĆ TEORETYCZNA: Kryptografia Stosowana & Biały Wywiad

### 1. Hash vs Szyfr – Podstawowa różnica architektoniczna
Zwykły użytkownik myśli, że haker „łamie hasło na Facebooku”. Jako specjaliści IT musicie wiedzieć, że to mit. Największe ataki to kradzież bazy danych z serwera (np. poprzez SQL Injection lub wyciek kopii zapasowej z chmury AWS).

Żadna profesjonalna firma **nie przechowuje haseł otwartym tekstem**. Stosuje się tzw. **funkcje skrótu (kryptograficzne hashowanie)**:
* **Szyfrowanie (np. AES-256, RSA):** Jest operacją **dwukierunkową**. Tekst jawny zamieniamy w szyfrogram za pomocą klucza, a posiadacz klucza może go w 100% odkodować.
* **Hashowanie (np. SHA-256, bcrypt):** Jest operacją **ściśle jednokierunkową (stratną matematycznie)**. Zamienia dowolnie długi ciąg (od jednej litery po obraz płyty DVD 4.7 GB) w stały skrót (256 bitów / 64 znaki hex). **Nie istnieje funkcja odwrotna `sha256_decrypt()`!**

### 2. Jak działa weryfikacja logowania?
1. Użytkownik rejestruje się z hasłem `TajneHaslo123`.
2. Serwer natychmiast liczy skrót: `sha256("TajneHaslo123")` &rarr; `e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855`.
3. Do bazy danych trafia wyłącznie ten skrót. Serwer „zapomina” tekst jawny hasła!
4. Przy kolejnym logowaniu serwer ponownie haszuje wpisany ciąg i porównuje hashe. Jeśli są identyczne – użytkownik zostaje zalogowany.

### 3. Tęczowe Tablice (Rainbow Tables) i Rola Soli (Salt)
Ponieważ funkcja skrótu jest deterministyczna, hash hasła `admin` to zawsze ten sam ciąg. Przestępcy przygotowali gigantyczne bazy danych (terabajty) z gotowymi parami: `[tekst jawny -> hash]` dla miliardów popularnych słów. Nazywamy je **Tęczowymi Tablicami (Rainbow Tables)**.

**Rozwiązanie: Sól Kryptograficzna (Salt)**  
Przed obliczeniem hasha serwer losuje unikalny ciąg (np. 16 bajtów losowych):
```python
import secrets
sol = secrets.token_hex(16) # np. '9a4f2b1c8e7d6a5f'
bezpieczny_hash = sha256(haslo + sol)
```
Sól zapisywana jest jawnie w bazie obok hasha. Dzięki temu haker nie może użyć gotowej tęczowej tablicy – musiałby wygenerować miliardy hashów od nowa dla każdego użytkownika z osobna!

### 4. Dlaczego SHA-256 jest za szybki dla haseł?
Pojedyncza nowoczesna karta graficzna **NVIDIA RTX 4090** potrafi przeliczyć ponad **8 miliardów operacji SHA-256 na sekundę**. Oznacza to, że 8-znakowe hasło ze słownika zostanie odgadnięte w kilka minut.  
Dlatego do haseł stosuje się tzw. **wolne funkcje wyprowadzania klucza (KDF)**, które celowo obciążają procesor i pamięć RAM:
* **bcrypt** (regulowany koszt obliczeniowy),
* **Argon2id** (zwycięzca Password Hashing Competition – wymaga dużej ilości RAM, blokując koparki ASIC),
* **PBKDF2**.

### 5. Czym jest Biały Wywiad (OSINT)?
**OSINT (Open-Source Intelligence)** to sztuka pozyskiwania informacji wywiadowczych ze źródeł jawnych i publicznie dostępnych.  
Audytorzy Red Team wykorzystują OSINT do:
* Mapowania struktury organizacji (kto jest dyrektorem, kto księgowym na LinkedIn),
* Badania wycieków z przeszłości w serwisach takich jak **DeHashed** czy **HaveIBeenPwned**,
* Wyszukiwania przypadkowo wystawionych serwerów za pomocą **Google Dorking** (`filetype:env`, `inurl:admin`).

---

# 💻 TUTORIAL W GOOGLE COLAB (Kod do Przećwiczenia na Lekcji)

1. Otwórz [Google Colab](https://colab.research.google.com).
2. Dodaj nową komórkę z kodem i wklej poniższy skrypt:

```python
import hashlib
import secrets

def stworz_hash_z_sola(haslo, sol=None):
    """
    Profesjonalna funkcja haszująca z obsługą soli kryptograficznej.
    """
    if sol is None:
        # Generujemy kryptograficznie bezpieczną sól (16 bajtów = 32 znaki hex)
        sol = secrets.token_hex(16)
    
    # Krok 1: Łączenie hasła z solą (tzw. salting)
    ciag_do_hashowania = (haslo + sol).encode('utf-8')
    
    # Krok 2: Zastosowanie algorytmu SHA-256
    obiekt_hash = hashlib.sha256(ciag_do_hashowania)
    skrot_hex = obiekt_hash.hexdigest()
    
    return skrot_hex, sol

# --- TESTOWANIE SILNIKA KRYPTOGRAFICZNEGO ---
haslo_testowe = "INFOTECH_2026"
hash1, sol1 = stworz_hash_z_sola(haslo_testowe)
hash2, sol2 = stworz_hash_z_sola(haslo_testowe)

print(f"Hasło: {haslo_testowe}")
print(f"Hash 1 (Sól: {sol1}):\n-> {hash1}\n")
print(f"Hash 2 (Sól: {sol2}):\n-> {hash2}\n")
print("Wniosek: To samo hasło dało dwa całkowicie odmienne hashe dzięki unikalnej soli!")
```

3. Uruchom komórkę (`Play`). Zobacz, jak zmienia się wynik i dlaczego unikalna sól całkowicie unieszkodliwia Tęczowe Tablice.

---

# 🎯 ZADANIE PROJEKTOWE DO ODDANIA (Google Classroom)
**Temat zadania w Classroomie:** *Projekt Red Team: Silnik Hashujący z Pętlą & Raport Wywiadowczy OSINT*  
**Forma:** Notatnik Colab + Raport analityczny

---

### 📌 Treść polecenia dla Nauczyciela (Do wklejenia w Google Classroom):
```markdown
# ⚡ PROJEKT: Kryptografia w Pythonie (SHA-256 z Solą) & Raport OSINT
Profil: Technikum Informatyczne / Programistyczne
Platforma: Google Classroom / Google Colab

DRODZY PRZYSZLI INŻYNIEROWIE IT!
W tym tygodniu działacie jako zespół audytorów bezpieczeństwa (Red Team). Waszym celem jest stworzenie skryptu automatyzującego hashowanie w chmurze oraz zbadanie realnego polskiego wycieku danych.

---
### 🛠️ MISJA 1: Python Hash Engine z pętlą FOR (Google Colab)
1. Otwórz notatnik w Google Colab i zaimportuj moduł `hashlib` oraz `secrets`.
2. Zdefiniuj listę przynajmniej 4 popularnych haseł: `["admin", "123456", "qwerty", "haslo123"]`.
3. Napisz pętlę `for`, która przeiteruje po liście i dla każdego hasła:
   - Wygeneruje losową sól,
   - Obliczy hash SHA-256 połączenia `haslo + sol`,
   - Wydrukuje czytelną tabelę wynikową w konsoli.
4. Kliknij w Colabie przycisk "Udostępnij" (Share) -> Zmień na: "Każda osoba mająca link może wyświetlać" i skopiuj adres URL.

---
### 🔍 MISJA 2: Raport Wywiadowczy OSINT (Afera Morele lub ALAB)
Korzystając z legalnych źródeł branżowych (Niebezpiecznik.pl, ZaufanaTrzeciaStrona.pl, CERT Polska):
1. Wybierz jeden głośny wyciek danych w Polsce:
   - Wariant A: Afera sklepu Morele.net (2,2 mln klientów, 2018 r.)
   - Wariant B: Atak ransomware na laboratoria medyczne ALAB (2023 r.)
2. Zbierz dane:
   - W jaki sposób napastnicy uzyskali dostęp (wektor ataku)?
   - Jakie wrażliwe kategorie danych (oprócz haseł) wyciekły?
   - Jakie skutki prawne i społeczne wywołał ten incydent?

---
### 📊 KRYTERIA OCENY (NaCoBeZu):
- Ocena Dostateczna (3): Poprawne hashowanie pojedynczego hasła w Colabie (działający link).
- Ocena Dobra (4): Działająca pętla for po liście haseł z solą + zwięzły raport OSINT (min. 3 zdania).
- Ocena Bardzo Dobra (5): Ocena 4 + elegancki, skomentowany kod w Colabie + wyczerpujący raport OSINT ze studium przypadku (skutki RODO, ryzyko spoofingu).
- Ocena Celująca (6) - Wyzwanie Architekta: Zaimplementowanie w Colabie funkcji sprawdzającej efekt lawinowy (skrypt porównujący dwa hashe różniące się 1 bitem i zliczający liczbę odmiennych znaków hex) LUB symulacji ataku słownikowego!
```

---

### ✍️ Formularz Odpowiedzi dla Ucznia (Do skopiowania i uzupełnienia w Classroom):
```text
--- FORMULARZ ODPOWIEDZI UCZNIA (Wklej do Google Classroom) ---
Imię i Nazwisko: [TWOJE IMIĘ I NAZWISKO]
Klasa / Profil: [NP. 2TI TECHNIKUM PROGRAMISTYCZNE]
Data wykonania: [RRRR-MM-DD]

1. LINK DO NOTATNIKA GOOGLE COLAB (MISJA 1):
- [Wklej publiczny link do notatnika Colab z uprawnieniem do odczytu]:
  https://colab.research.google.com/drive/...

2. FRAGMENT KLUCZOWEGO KODU PYTHON (Pętla for z soleniem):
```python
# [Wklej tutaj kod swojej pętli for z Colaba]
import hashlib
import secrets

hasla = ["admin", "123456", "qwerty", "Tajne2026!"]
for h in hasla:
    # Twoja pętla...
```

3. RAPORT WYWIADOWCZY OSINT (MISJA 2):
- Wybrany incydent: [Morele.net 2018 / ALAB Laboratoria 2023]
- Wektor ataku / Przyczyna incydentu: 
  [WPISZ TUTAJ: np. Atak ransomware grupy RA World, przełamanie uwierzytelniania, luka w panelu...]
- Jakie dane dostały się w ręce przestępców oprócz haseł?:
  [WPISZ TUTAJ: np. Numery PESEL, telefony, adresy zamieszkania, wyniki badań medycznych...]
- Dlaczego samo hashowanie haseł nie uchroniło klientów przed atakami phishingowymi?:
  [WPISZ TUTAJ: np. Przestępcy wykorzystali numery telefonów do wysyłania targetowanych SMS-ów z wezwaniem do dopłaty...]

4. WYZWANIE NA OCENĘ CELUJĄCĄ (6) - OPCJONALNE:
- [Opis implementacji funkcji zliczającej efekt lawinowy lub symulacji ataku słownikowego w Colabie]: ...
----------------------------------------------------------------
```
