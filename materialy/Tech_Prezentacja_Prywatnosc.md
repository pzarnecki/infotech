# SZKOLENIE ZAAWANSOWANE: Architektura Prywatności (Technikum)
*Format: Prezentacja szkoleniowa i wprowadzenie do Qubes OS*

***

## SLAJD 1: Złudzenie prywatności – Tryb Incognito to tylko mit
- **Mechanika:** Tryb incognito nie zapisuje sesji (Local Storage/Cookies) lokalnie na dysku twardym klienta. Nie zostawia śladów dla innych użytkowników OS (np. rodziny).
- **Zagrożenie:** ISP (Internet Service Provider), administrator sieci (szkoła/kawiarnia) oraz router wciąż widzą żądania DNS w postaci jawnej oraz komunikację HTTP. Strony i trackery wciąż rozpoznają Cię poprzez tzw. **Browser Fingerprinting** (unikalny sprzęt, rozdzielczość ekranu, zainstalowane czcionki).

***

## SLAJD 2: Filtrowanie Sieci: AdBlock vs Pi-Hole
- **AdBlock w przeglądarce:** Rozszerzenia (np. uBlock Origin) blokują żądania na poziomie DOM przeglądarki. Filtrują złośliwe i śledzące skrypty (trackery analizujące ruch myszki, czas na stronie).
- **DNS Sinkhole (np. Pi-Hole):** Bardziej zaawansowana architektura. Stawiamy mały serwer (np. na Raspberry Pi) na poziomie routera. Wszystkie żądania z całej sieci do domen serwujących reklamy "wpadają w czarną dziurę" (zwracany jest adres 0.0.0.0), dzięki czemu reklamy znikają z każdego sprzętu, zanim w ogóle dotrą do urządzenia.

***

## SLAJD 3: VPN – Kto ma klucze do tunelu?
- **Protokół szyfrujący:** VPN (np. WireGuard, OpenVPN) zamyka Twoje pakiety w szyfrowanym tunelu między Twoją kartą sieciową a zdalnym serwerem.
- **Kwestia zaufania:** Haker i ISP nie widzą Twojego ruchu, ale... FIRMA OFERUJĄCA VPN WIDZI WSZYSTKO. Dlatego darmowe VPN-y to często oszustwo – sprzedają logi Twojego ruchu. Jeśli korzystasz z VPN, firma musi mieć certyfikaty "No-Logs Policy" audytowane przez podmioty trzecie.

***

## SLAJD 4: The Onion Router (Sieć TOR)
- **Topologia sieci:** Router Cebulowy nie ufa jednemu serwerowi centralnemu. Twój klient szyfruje pakiet trzykrotnie (jak 3 warstwy cebuli).
- **Odbijanie:** Pakiet wędruje przez 3 losowo dobrane węzły (Entry Node, Relay Node, Exit Node).
- **Architektura:** Węzeł przekaźnikowy odszyfrowuje tylko 1 warstwę – wie, skąd pakiet przyszedł, i do kogo go podać, ale nie wie, co jest w środku ani kto był pierwotnym nadawcą. Jedynie węzeł wyjściowy (Exit Node) "zdejmuje" ostatnią warstwę i wysyła pakiet w jawny internet. Dlatego ruch przez węzeł wyjściowy musi być chroniony przez HTTPS!

***

## SLAJD 5: System QUBES OS – Bezpieczeństwo poprzez separację (Pokaz zjawiska)
- **Problem Monolitów:** Windows i MacOS to systemy monolityczne. Jeśli klikniesz złośliwy link w przeglądarce pobierając wirusa, wirus ma potencjalny dostęp do Twojego pulpitu i folderu z dokumentami.
- **Odpowiedź - Qubes OS:** Uznawany za najbezpieczniejszy system na świecie. Wykorzystuje zaawansowaną wizualizację (Xen Hypervisor).
- **Działanie (Izolacja):** Qubes dzieli Twoje życie na odseparowane maszyny wirtualne (tzw. "Qubes" - kostki). Masz oddzielny serwer sieciowy, oddzielny Qube do przeglądania internetu prywatnego (np. w czerwonej ramce), oddzielny do banku (zielona ramka).
- **Złośliwy link:** Jeśli pobierzesz wirusa w "czerwonym" Qube, infekuje on TYLKO ten jeden kontener. Twój Qube bankowy i pliki prywatne są fizycznie (architektonicznie) odizolowane, jakby działały na osobnym komputerze na biurku. Zamykasz zainfekowany "Qube" i problem znika!
