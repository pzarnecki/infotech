# ZAAWANSOWANE PRAWO W IT (Technikum)
*Materiały do zblokowanych zajęć 4-5: Licencjonowanie, Prawa Autorskie i Etyka AI w Developmencie*

***
## SLAJD 1: Kto jest właścicielem Twojego Kodu?
- Jako programista, Twój kod to Twoja własność intelektualna (IP). Prawa majątkowe do kodu napisanego "po godzinach" należą do Ciebie. Prawa majątkowe do kodu napisanego w pracy na umowę o pracę należą domyślnie do pracodawcy.
- **GitHub to nie Domena Publiczna!** Kod wrzucony na GitHuba bez podpiętego pliku `LICENSE` wciąż podlega pełnemu prawu autorskiemu (All Rights Reserved). Oznacza to, że pomimo tego, iż kod jest widoczny publicznie, nikt nie ma prawa go skopiować bez Twojej wyraźnej, pisemnej zgody!

***
## SLAJD 2: Open Source (Model biznesowy a idea)
- Open Source to nie tylko darmowy kod, to cały model tworzenia oprogramowania (m.in. jądro Linuxa).
- **Rodzina Permissive (np. Licencja MIT, Apache 2.0):** Robisz z kodem co chcesz. Możesz wziąć darmowy kod, zmodyfikować go, skompilować i sprzedawać w zamkniętym programie. Musisz tylko dodać notkę o oryginalnym twórcy. (Dlatego wielkie korporacje uwielbiają licencję MIT).
- **Rodzina Copyleft (np. Licencja GPL, AGPL):** Nazywana "wirusem licencyjnym". Pozwala używać kodu za darmo, ale wymusza, aby JAKIKOLWIEK program zbudowany z użyciem tego kodu, również został wydany na darmowej, otwartej licencji GPL. (To mechanizm chroniący przed tym, by korporacje nie zamykały darmowej pracy społeczności).

***
## SLAJD 3: Piractwo i Inżynieria Wsteczna (Reverse Engineering)
- Dekompilacja programu komercyjnego i sprzedawanie go pod inną nazwą to kradzież własności intelektualnej.
- Z punktu widzenia bezpieczeństwa (Audyty IT), **White Hat Hackers** prowadzą inżynierię wsteczną oprogramowania, aby szukać dziur (np. zgłaszając je w programach Bug Bounty) - co czasami balansuje na granicy regulaminów oprogramowania (EULA), ale jest akceptowane rynkowo w celach badawczych.

***
## SLAJD 4: Etyka AI – Prawne bagno GitHub Copilot
- **Jak uczą się LLM?** Modele takie jak ChatGPT czy Copilot trenowały na repozytoriach GitHuba.
- **Problem prania licencji (License Laundering):** AI uczy się na kodzie z licencją GPL. Gdy Ty prosisz AI o napisanie funkcji, model często "wypluwa" dokładnie ten sam kod z licencji GPL, ale bez notatki licencyjnej! Ty wklejasz go do swojego zamkniętego, komercyjnego programu i... nieświadomie łamiesz prawo i grozi Ci pozew. 
- Zjawisko to sprowadziło na wielkie firmy (OpenAI, Microsoft, Stability AI) zbiorowe pozwy od wściekłych artystów i programistów. Pamiętaj: Ty bierzesz odpowiedzialność za kod wrzucony do projektu, nawet jeśli napisało go AI.
