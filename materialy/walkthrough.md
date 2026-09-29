# Podsumowanie: Materiały na pierwsze 2 miesiące

Wygenerowano **31 plików dla uczniów** + **31 plików źródłowych (.md) dla nauczyciela**.

## Struktura plików na Nextcloud

```
Techninikum_Liceum/
├── Rozklady_Materialu/
│   └── rozklad_dla_dyrekcji.pdf
│
├── Liceum/  (8 lekcji = ~2 miesiące przy 1h/tyg)
│   ├── Lekcja_01_Wstep_Cloud/
│   │   ├── LO_L01_Prezentacja.pptx    ← rzutnik
│   │   ├── LO_L01_Tutorial.pdf        ← do czytania
│   │   └── LO_L01_Zadania.docx        ← uczeń edytuje
│   ├── Lekcja_02_03_Cyberbezpieczenstwo/
│   │   ├── LO_L02_03_Prezentacja.pptx
│   │   ├── LO_L02_03_Tutorial.pdf
│   │   ├── LO_L02_03_Zadania.docx
│   │   └── LO_L04_Zadanie_Podsumowujace.docx  ← wyzwanie co 3 lekcje
│   ├── Lekcja_04_05_Prawo_IT/
│   │   ├── LO_L04_05_Prezentacja.pptx
│   │   ├── LO_L04_05_Tutorial.pdf
│   │   └── LO_L04_05_Zadania.docx
│   ├── Lekcja_06_Procesor_Tekstu/
│   │   ├── LO_L06_Prezentacja.pptx
│   │   ├── LO_L06_Tutorial.pdf
│   │   └── LO_L06_Zadania.docx
│   └── Lekcja_07_08_Arkusz/
│       ├── LO_L07_08_Prezentacja.pptx
│       ├── LO_L07_08_Tutorial.pdf
│       └── LO_L07_08_Zadania.docx
│
├── Technikum/  (8 bloków 2h = ~2 miesiące przy 2h/tyg)
│   ├── Lekcja_01_Wstep_Cloud/
│   │   ├── Tech_L01_Prezentacja.pptx
│   │   ├── Tech_L01_Tutorial.pdf
│   │   └── Tech_L01_Zadania.docx
│   ├── Lekcja_02_03_Cyber_OSINT/
│   │   ├── Tech_L02_03_Prezentacja.pptx
│   │   ├── Tech_L02_03_Tutorial.pdf
│   │   └── Tech_L02_03_Zadania.docx
│   ├── Lekcja_04_05_Prawo_IT/
│   │   ├── Tech_L04_05_Prezentacja.pptx
│   │   ├── Tech_L04_05_Tutorial.pdf
│   │   └── Tech_L04_05_Zadania.docx
│   ├── Lekcja_06_Procesor_Tekstu/
│   │   ├── Tech_L06_Prezentacja.pptx
│   │   ├── Tech_L06_Tutorial.pdf
│   │   └── Tech_L06_Zadania.docx
│   └── Lekcja_07_08_Arkusz/
│       ├── Tech_L07_08_Prezentacja.pptx
│       ├── Tech_L07_08_Tutorial.pdf
│       └── Tech_L07_08_Zadania.docx
│
└── Nauczyciel_MD/  (31 plików .md – edytowalne źródła)
```

## Formaty plików – Jak ich używać

| Format | Przeznaczenie | Jak używasz |
|---|---|---|
| **.pptx** (Prezentacja) | Wyświetlasz na rzutniku na lekcji | Otwórz w PowerPoint / Google Slides / LibreOffice |
| **.pdf** (Tutorial/Skrypt) | Materiał do czytania dla uczniów | Wrzuć jako załącznik w Google Classroom |
| **.docx** (Karta Zadań) | Uczeń edytuje, wpisuje odpowiedzi i oddaje | Wrzuć w Classroom jako "Utwórz kopię dla każdego ucznia" |

## Zawartość merytoryczna – co zostało uwzględnione

### LICEUM (od absolutnych podstaw)
- **L01:** Cloud computing, Google Colab, Hello World
- **L02-03:** Hasła, 2FA (SMS vs Authenticator), wycieki, phishing, social engineering (pretexting, baiting, tailgating), prywatność (Incognito – mit!, VPN, AdBlock/uBlock, TOR)
- **L04:** Zadanie podsumowujące (HaveIBeenPwned + analiza fałszywego SMS-a + fałszywa strona banku)
- **L04-05:** Prawo autorskie, GitHub, licencje MIT/GPL, Creative Commons (CC-BY, CC-BY-NC), RODO/GDPR, piractwo, etyka AI, deepfake
- **L06:** Google Docs, NotebookLM (AI do syntezy źródeł), formatowanie dokumentacji
- **L07-08:** Arkusz kalkulacyjny: "brudne dane", SUMA, ŚREDNIA, JEŻELI, VLOOKUP, wykresy

### TECHNIKUM (zaawansowane, analityczno-security)
- **L01:** Cloud (IaaS/PaaS/SaaS), Colab/Jupyter, OSINT wstęp, ślad cyfrowy
- **L02-03:** SHA-256 vs MD5 vs bCrypt, Salt, Rainbow Tables, Brute Force vs Dictionary, skrypt Python hashlib, OSINT (whois, Shodan, Google Dorking), prywatność (Browser Fingerprinting, WireGuard, Pi-Hole/DNS Sinkhole, TOR Exit Node), social engineering z AI (jailbreaking LLM)
- **L04-05:** Własność IP kodu, MIT/Apache/GPL/AGPL/LGPL, NDA, RODO dla developerów, EU AI Act, License Laundering (Copilot), Bug Bounty, Reverse Engineering, Qubes OS
- **L06:** Dokumentacja techniczna (README.md, specyfikacja), Markdown, NotebookLM, praca zespołowa w Docs
- **L07-08:** Import CSV/JSON, TRIM/CLEAN, VLOOKUP + INDEKS/PODAJ.POZYCJĘ, tabele przestawne (Pivot), sparklines, formatowanie warunkowe, analiza logów serwera, kiedy arkusz vs pandas
