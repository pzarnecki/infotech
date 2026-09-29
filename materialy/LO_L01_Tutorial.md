# Wstęp do chmury obliczeniowej: Praca, Backup i Sztuczna Inteligencja

Witaj na pierwszej lekcji! Dzisiaj zanurzymy się w świat IT i dowiemy się, jak pracują nowocześni analitycy, programiści oraz menedżerowie. Wszystko, co dzisiaj robimy, dzieje się "w chmurze". 

## 1. Czym jest Cloud Computing? W chmurze uruchomisz WSZYSTKO

Wyobraź sobie, że potrzebujesz bardzo mocnego komputera do wyrenderowania filmu albo uruchomienia najnowszej gry, ale masz tylko stary laptop z 4GB RAM-u. Zamiast kupować drogi sprzęt, możesz wynająć jego moc przez Internet. To właśnie istota chmury obliczeniowej (Cloud Computing).

W chmurze nie trzymasz tylko "plików i zdjęć". W chmurze możesz uruchomić **dosłownie wszystko**:
- **Oprogramowanie (SaaS):** Google Docs czy Microsoft 365. Zamiast instalować Worda, odpalasz go w przeglądarce.
- **Wirtualne Komputery (IaaS):** Możesz wynająć cały system Windows lub Linux, który fizycznie stoi w serwerowni w Irlandii, ale Ty widzisz jego pulpit na swoim monitorze w domu.
- **Gry (Cloud Gaming):** Usługi takie jak NVIDIA GeForce NOW pozwalają grać w gry na "ultra" detalach na słabym komputerze – gra uruchamia się w chmurze, a Ty dostajesz tylko strumień wideo (jak na YouTube), do którego wysyłasz kliknięcia myszką.

## 2. Wymiana plików i potęga Backupu

Skoro wszystko przenosimy do chmury (Google Drive, OneDrive), musimy umieć z tego bezpiecznie korzystać.

### Współdzielenie (Udostępnianie)
W IT rzadko wysyłamy pliki jako "załączniki" do maila. Zamiast tego wysyłamy **link do pliku w chmurze**. 
- **Dostęp przez link:** Każdy, kto kliknie, widzi plik. (Dobre do publicznych materiałów).
- **Dostęp z restrykcją:** Tylko konkretny e-mail (np. szefa) ma prawo otworzyć plik. Jeśli wyślesz link komuś innemu – odbije się od ściany logowania. 
W chmurze na jednym pliku może pracować np. 10 osób jednocześnie, widząc swoje kursory na żywo!

### Backup (Kopia zapasowa)
"Ludzie dzielą się na tych, którzy robią backupy, i tych, którzy będą je robić" (gdy stracą dane).
Zapisywanie plików w chmurze (Google Drive) to rodzaj automatycznego backupu (autosave). Nawet jeśli na Twoim komputerze spali się dysk, dane wciąż są bezpieczne na serwerach firmy zewnętrznej. 
*Złota zasada IT to 3-2-1:* 3 kopie danych, na 2 różnych nośnikach (np. dysk i pendrive), w tym 1 kopia w chmurze (off-site).

## 3. Narzędzie nr 1: Google Colab – nasz warsztat kodu

W IT często trzeba szybko coś zautomatyzować. Nie będziemy instalować języka Python na dysku. Użyjemy chmury.

**Google Colab** to darmowy notatnik (Jupyter Notebook) działający w chmurze. Umożliwia pisanie i uruchamianie kodu bezpośrednio z przeglądarki!
Składa się on z:
- **Komórek tekstowych** (do notatek).
- **Komórek z kodem** (do instrukcji dla komputera).

**Twój pierwszy kod**
Wpisz to w komórce z kodem w Colabie:
```python
print('Hello World')
```
Gdy naciśniesz "Play", potężne serwery Google przetworzą tę linijkę i odeślą Ci wynik. Właśnie napisałeś swój pierwszy skrypt!

## 4. Narzędzie nr 2: NotebookLM (Notebook Gemini) – Twój asystent analityczny

Programowanie to ułamek pracy w IT. Znacznie częściej musisz zanalizować ogromną ilość informacji (np. dokumentację na 200 stron). Do tego posłuży nam chmurowa sztuczna inteligencja: **Notebook Gemini**.

Różni się on diametralnie od zwykłego ChatGPT. Zwykły chatbot często "zmyśla" (tzw. halucynacje), bo próbuje zgadnąć odpowiedź ze swojej bazy wiedzy. 

**Jak działa Notebook Gemini?**
1. **Tworzysz Notatnik i wgrywasz źródła:** np. pliki PDF, linki do stron WWW, dokumenty Google, filmy z YouTube.
2. **Zamknięty ekosystem:** Gemini analizuje **TYLKO** to, co wgrałeś. Traktuje wgrane pliki jak "prawdę objawioną".
3. **Analiza i przypisy:** Zadajesz pytanie, np. *"Jakie są kluczowe kroki w procedurze ewakuacji opisanej w tym 50-stronicowym dokumencie?"*. Gemini generuje odpowiedź i dodaje **przypisy**. Jeśli klikniesz przypis nr 1, Gemini przeniesie Cię do konkretnej strony w PDF-ie, żeby udowodnić Ci, skąd wziął informację!
4. **Zastosowanie w szkole i pracy:** Nie używaj AI do pisania wypracowań z niczego. Używaj Gemini do: podsumowywania notatek, tłumaczenia trudnych tekstów, generowania fiszek do nauki z Twoich własnych plików i szukania luk w dokumentacji projektowej. Opanowanie tego narzędzia da Ci ogromną przewagę na rynku!
