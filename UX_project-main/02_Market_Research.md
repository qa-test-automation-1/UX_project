# TaskFlow — Market Research & Competitive Analysis

> **Status dokumentu:** analiza wtórna (desk research), stan na 8 listopada 2026 r.  
> **Zakres:** rynek aplikacji do codziennych zadań, pięciu wskazanych konkurentów oraz rekomendacje dla koncepcyjnego MVP TaskFlow.  
> **Ważne:** TaskFlow jest projektem koncepcyjnym. Profile i odpowiedzi przedstawione w `02_User_Research.md` są syntetyczne, a nie zebrane od rzeczywistych respondentów. Wnioski z tego dokumentu nie są walidacją rynkową ani wynikiem testów użyteczności.

## 1. Executive Summary

Rynek aplikacji To-Do obejmuje zarówno proste listy zadań, jak i rozbudowane systemy planowania, kalendarze, współdzielenie oraz narzędzia skupienia. W analizowanej grupie konkurentów widać dwa użyteczne krańce: Microsoft To Do i Google Tasks oferują bezpłatne, powiązane z ekosystemami rozwiązania; Todoist, TickTick i Any.do rozwijają szersze zestawy funkcji z warstwą płatną. To obserwacja porównawcza, nie pomiar udziałów rynkowych.

Założenie projektu TaskFlow — szybkie dodanie zadania, czytelna lista „Dzisiaj”, widoczne priorytety i jednoznaczne ukończenie — celuje w częsty, podstawowy przepływ użycia. Sam prosty interfejs nie jest jednak unikalną przewagą: konkurenci również mają szybkie dodawanie, widok dnia, terminy, synchronizację i darmowy plan. Potencjalnym wyróżnikiem może być świadomie ograniczony zakres MVP oraz bardzo niski koszt poznawczy: najpierw zadanie, termin/priorytet i wykonanie, bez wymuszania budowania skomplikowanego systemu.

Rekomendowany MVP: tworzenie i edycja zadania, widok „Dzisiaj”, lista „Zaległe”, podstawowe priorytety, proste terminy/przypomnienia, powtarzanie, podzadania, wyszukiwanie lub proste filtrowanie, synchronizacja i dostępność podstawowych operacji z klawiatury. Kalendarz rozbudowany, automatyzacje, AI, współpraca zespołowa, habit tracker i statystyki należy odłożyć.

## 2. Research Objectives

- Opisać kategorie rozwiązań obecnych w aplikacjach To-Do.
- Porównać wybrane produkty pod względem funkcji, modelu biznesowego, platform i przepływu dodania zadania.
- Wskazać obszary, w których koncepcyjny TaskFlow może być prostszy i bardziej spójny.
- Przełożyć ustalenia na ograniczony zakres MVP, priorytety MoSCoW oraz hipotezy do walidacji.

## 3. Research Methodology

### Metoda

Desk research oparty przede wszystkim na publicznych stronach cenowych, stronach funkcji i oficjalnych centrach pomocy producentów, a także na standardzie WCAG 2.2. Informacje o cenach i limitach mogą się zmieniać; przed wdrożeniem modelu biznesowego należy sprawdzić je ponownie dla polskiego regionu i waluty.

### Zasady interpretacji

- **Fakt** — informacja opublikowana przez producenta lub W3C; odniesienie znajduje się w sekcji Sources & References.
- **Ocena UX** — ekspercka interpretacja publicznie opisanych przepływów i funkcji, a nie wynik moderowanego testu.
- **Rekomendacja** — propozycja projektowa dla TaskFlow, wymagająca walidacji z użytkownikami.
- **Brak danych** — cecha, której nie da się rzetelnie potwierdzić w źródłach wykorzystanych w tej analizie. Brak danych nie oznacza braku funkcji.

### Ograniczenia

- Nie przeprowadzono testów konkurencyjnych aplikacji na kontach użytkowników ani audytu ich kodu.
- Ocena UI nie obejmuje pełnego zestawu ekranów, urządzeń, stanów ani lokalizacji językowych.
- Dostępna dokumentacja projektu TaskFlow opisuje kierunek funkcjonalny, ale nie zawiera w tym badaniu zweryfikowanego, interaktywnego prototypu do testowania.
- `02_User_Research.md` opisuje pięć fikcyjnych profili. Są one materiałem ćwiczeniowym i nie stanowią źródła dowodów o populacji użytkowników.
- Nie znaleziono wiarygodnych, porównywalnych danych liczbowych o wielkości rynku, udziałach rynkowych ani popularności produktów; dokument ich nie szacuje.

## 4. Market Overview

### 4.1 Charakterystyka rynku To-Do

Aplikacje To-Do konkurują o codzienny przepływ: **przechwycenie zadania → nadanie kontekstu → decyzja, co zrobić teraz → wykonanie → ponowne zaplanowanie lub zamknięcie**. Produkty różnią się stopniem rozbudowania: od list i integracji z pocztą/kalendarzem po wiele widoków, filtrowanie, współpracę, nawyki i techniki koncentracji. Przykłady funkcji opisane przez producentów obejmują szybkie dodawanie, priorytety, przypomnienia, zadania cykliczne, podzadania, kalendarze i synchronizację między platformami [1–5].

### 4.2 Potrzeby i problemy użytkowników

Poniższe punkty są syntezą celów produktu i analizowanych funkcji, a nie pomiarem częstości problemów:

- **Szybkie przechwycenie:** zapisanie myśli bez rozbudowanego formularza. Todoist i TickTick opisują szybkie dodawanie, również z datą wprowadzoną językiem naturalnym [1, 3].
- **Orientacja na dziś:** ograniczenie listy do zadań istotnych w danym momencie. Microsoft To Do promuje widok „My Day” i sugestie zadań [9]; Any.do opisuje „My Day” w planie bezpłatnym [7].
- **Rozróżnienie ważności i terminu:** priorytety, terminy oraz przypomnienia występują u kilku konkurentów [1–5].
- **Ograniczenie przeciążenia:** coraz więcej widoków i opcji zwiększa możliwości, ale może wymagać od użytkownika decyzji konfiguracyjnych. To hipoteza UX do sprawdzenia, nie stwierdzony rezultat badań.
- **Ciągłość między urządzeniami:** analizowane produkty komunikują synchronizację lub dostępność na wielu platformach [1–5].
- **Dostępność i obsługa klawiaturą:** WCAG 2.2 zawiera kryteria m.in. dotyczące kontrastu, widoczności fokusu i minimalnego rozmiaru celów interakcji [11].

### 4.3 Trendy produktowe i projektowe zaobserwowane w źródłach

- **Quick Add i natural-language input:** rozpoznawanie dat, godzin i metadanych podczas wpisywania zadania [1, 3].
- **Widoki dopasowane do pracy:** lista, tablica, kalendarz, a w TickTick również oś czasu [1, 3].
- **Planowanie dzienne i ponowne proponowanie zadań:** przykład Microsoft To Do „My Day” [9].
- **Integracje z ekosystemem:** Google Tasks pozwala tworzyć zadania z usług Google Workspace, m.in. Gmaila i Kalendarza [4].
- **Rozszerzanie produktu poza listę:** TickTick wymienia Pomodoro, nawyki, statystyki i macierz Eisenhowera [3].
- **Funkcje AI i głosowe:** strony Todoist, TickTick i Any.do opisują wybrane funkcje asystujące lub wejście głosowe [1, 3, 6]. To sygnał kierunku ofert, nie dowód powszechnego popytu.
- **Responsywność i platformy:** produkty oferują aplikacje webowe i mobilne; część także desktopowe, rozszerzenia lub urządzenia ubieralne [1–5].

### 4.4 Modele biznesowe

| Model | Przykład z analizowanej grupy | Konsekwencja dla użytkownika | Wniosek dla TaskFlow |
|---|---|---|---|
| Free | Microsoft To Do jest opisywany przez Microsoft jako bezpłatny; Google Tasks jest częścią usług Google [4, 5, 9]. | Podstawowy use case może być dostępny bez subskrypcji; wartość jest związana z ekosystemem. | Jeżeli aplikacja ma pozostać koncepcją portfolio, nie trzeba wybierać monetyzacji. Jeśli powstanie produkt, bezpłatny rdzeń powinien wystarczyć do codziennego użycia. |
| Freemium | Todoist, TickTick i Any.do mają bezpłatny poziom oraz płatne plany z rozszerzeniami lub wyższymi limitami [1, 2, 6–8]. | Użytkownik może zacząć bez płatności; część widoków, limitów lub zaawansowanych funkcji jest płatna. | Potencjalny model, jeśli później pojawią się kosztowne funkcje premium. Nie należy blokować podstawowego dodawania, wykonywania i przeglądania zadań. |
| Subscription | Płatne plany Todoist Pro, TickTick Premium i Any.do Premium są rozliczane jako subskrypcje [1, 2, 6, 8]. | Powtarzalna opłata za rozszerzone funkcje lub większe limity. | Hipoteza monetyzacji na dalszym etapie; wymaga rozmów o gotowości do zapłaty i analizy kosztów utrzymania. |

### 4.5 Potencjalne nisze i wyróżnienie TaskFlow

To możliwości do walidacji, a nie potwierdzone luki rynkowe:

1. **„Dziś bez konfiguracji”** — ekran startowy pokazujący zadania dzisiejsze i zaległe w czytelnym porządku.
2. **Szybkie dodawanie z rozsądnymi domyślnymi ustawieniami** — użytkownik zapisuje zadanie, a termin, priorytet i podzadania dodaje tylko wtedy, gdy są potrzebne.
3. **Widoczne, ale spokojne statusy** — odróżnienie „do zrobienia”, „dziś”, „zaległe” i „wykonane” bez polegania wyłącznie na kolorze.
4. **Kontrola nad przypomnieniami** — ustawienie przypomnienia w kontekście zadania i możliwość łatwego ograniczenia powiadomień.
5. **Polski, zrozumiały język interfejsu** — krótkie etykiety, czytelne komunikaty i brak konieczności poznawania składni filtrów.

## 5. Competitor Analysis

### 5.1 Todoist

- **Grupa docelowa — fakt:** produkt przedstawia się jako narzędzie do organizowania pracy i życia; obsługuje zadania osobiste i zespołowe [1].
- **Funkcje i model — fakt:** Quick Add, priorytety, etykiety, sekcje, podzadania, widoki listy i tablicy; plan Beginner jest bezpłatny, Pro rozszerza m.in. limity i widok kalendarza [1, 2]. Cennik w USD; nie należy traktować tej wartości jako ceny końcowej w Polsce.
- **Dodawanie — fakt:** Quick Add rozpoznaje m.in. datę, priorytet, etykietę i przypomnienie na podstawie wpisanej treści [10].
- **Organizowanie — fakt:** projekty/sekcje, priorytety, etykiety, filtry oraz widoki; kalendarz jest zależny od planu [1, 2, 10].
- **Platformy — fakt:** web, Windows, macOS, Linux, iOS, Android, Apple Watch/Wear OS oraz integracje z przeglądarką i pocztą [12].
- **Ocena UX — interpretacja:** bardzo szybki przepływ dla osób, które poznają skróty i składnię Quick Add; jednocześnie mnogość pojęć (projekty, sekcje, etykiety, filtry, priorytety) może zwiększać koszt wejścia dla osoby szukającej tylko krótkiej listy. Nie jest to wynik testu.
- **Potencjalna bariera — interpretacja:** użytkownik może nie wiedzieć, czy zadanie powinno trafić do projektu, sekcji czy filtra; funkcje i limity planów wymagają porównania przed wyborem.

### 5.2 Microsoft To Do

- **Grupa docelowa — fakt:** Microsoft opisuje narzędzie jako prostą listę osobistą, z widokiem dziennym, dodatkowymi listami oraz integracją z Outlook/Exchange [5, 9].
- **Funkcje i model — fakt:** „My Day”, sugestie, listy, terminy, przypomnienia, gwiazdki, kroki/podzadania i notatki; bezpłatne przy użyciu osobistego konta Microsoft, a konto służbowe wymaga odpowiedniej licencji [5, 9, 13].
- **Dodawanie — fakt:** zadanie można wpisać bezpośrednio w „My Day” lub innej liście; zadania z Outlooka można włączać do planowania dnia [9].
- **Organizowanie — fakt:** wiele list, widok dzienny, sugestie i udostępnianie list w obsługiwanych scenariuszach [9, 14].
- **Platformy — fakt:** web, Windows, Mac, iOS i Android [15].
- **Ocena UX — interpretacja:** „My Day” daje czytelny punkt startowy i pozwala oddzielić plan dnia od całego zbioru zadań. Wartość jest szczególnie czytelna dla użytkownika Outlooka; zależność od konta/ekosystemu może być mniej wygodna dla osób pracujących w innym środowisku. Nie jest to wynik testu.
- **Potencjalna bariera — interpretacja:** sugestie zadań i oddzielne listy wymagają zrozumienia, gdzie żyje zadanie i czy dodanie do dnia tworzy kopię czy planuje istniejące zadanie; szczegóły powinny być oceniane w aktualnej aplikacji.

### 5.3 TickTick

- **Grupa docelowa — fakt:** producent kieruje produkt do planowania pracy, życia i nauki, z narzędziami organizacji i skupienia [3].
- **Funkcje i model — fakt:** plan bezpłatny obejmuje m.in. listy, widok listy i Kanban, przypomnienia, synchronizację oraz limit 9 list/99 zadań na listę; Premium według strony producenta kosztuje 49,99 USD rocznie i rozszerza limity oraz widoki kalendarza [6].
- **Dodawanie — fakt:** szybkie dodawanie, natural-language input, wejście głosowe, widgety i skrót desktopowy [3].
- **Organizowanie — fakt:** listy, tagi, filtry, priorytety, podzadania, powtarzanie, wiele widoków kalendarza, Kanban/timeline; również Pomodoro, nawyki i statystyki [3, 6].
- **Platformy — fakt:** aplikacja webowa oraz m.in. Android, Windows, Linux, macOS i iOS/iPadOS [16].
- **Ocena UX — interpretacja:** szeroki zestaw narzędzi pozwala skonfigurować wiele sposobów pracy; może jednak konkurować o uwagę z podstawową listą zadań. Jest dobrym benchmarkiem dla szybkiego dodawania i elastyczności, niekoniecznie dla minimalistycznego MVP. Nie jest to wynik testu.
- **Potencjalna bariera — interpretacja:** mnogość widoków i narzędzi może wymagać decyzji, których nie potrzebuje osoba planująca tylko prosty dzień; bezpłatny limit list/zadań może być ograniczeniem przy większym użyciu.

### 5.4 Google Tasks

- **Grupa docelowa — fakt:** Google opisuje Tasks jako prosty sposób śledzenia zadań z poziomu usług Google Workspace [4].
- **Funkcje i model — fakt:** tworzenie zadań z Gmaila, Kalendarza i innych usług Google, terminy, powiadomienia, listy, podzadania, zadania cykliczne i synchronizacja; brak osobnej płatnej warstwy Tasks opisanej w użytych materiałach [4, 17].
- **Dodawanie — fakt:** zadanie można dodać w Tasks, Kalendarzu lub z wiadomości Gmail; w mobilnym przepływie podstawowa ścieżka obejmuje przycisk dodawania, tytuł i zapis, a termin można doprecyzować [17].
- **Organizowanie — fakt:** listy, podzadania, gwiazdki i zadania cykliczne [4, 17].
- **Platformy — fakt:** web przez Kalendarz/Tasks oraz aplikacje mobilne; zadania synchronizują się na urządzeniach zalogowanych na to samo konto [4, 5].
- **Ocena UX — interpretacja:** mocną stroną jest niski próg wejścia i obecność w znanym ekosystemie Google. Prostota funkcji może być zaletą przy krótkich listach; osoby potrzebujące bardziej złożonych filtrów, wielu typów widoków lub rozbudowanego zarządzania mogą szukać narzędzia z szerszym zestawem funkcji. To interpretacja zakresu funkcji, nie test.
- **Potencjalna bariera — interpretacja:** wartość jest związana z kontem i usługami Google, a doświadczenie webowe jest rozproszone między Tasks i Kalendarzem.

### 5.5 Any.do

- **Grupa docelowa — fakt:** Any.do opisuje plan Personal jako organizację spraw osobistych, Premium jako produkt dla intensywnych użytkowników, Family dla gospodarstw domowych, a Teams dla współpracy [7].
- **Funkcje i model — fakt:** darmowy Personal obejmuje zadania i listy, przypomnienia, kalendarz, daily planner oraz synchronizację; płatne plany dodają m.in. zadania cykliczne, przypomnienia lokalizacyjne/WhatsApp, współdzielone przestrzenie lub funkcje zespołowe [7, 8].
- **Dodawanie — fakt:** Any.do opisuje wejście przez aplikację, widok My Day, integracje oraz wejście głosowe; szczegóły dostępności mogą zależeć od platformy i planu [8].
- **Organizowanie — fakt:** zadania, listy, kalendarz, widok dnia; bardziej rozbudowane współdzielenie i funkcje premium są przypisane do płatnych planów [7, 8].
- **Platformy — fakt:** web, desktop, iOS, Android, tablety, rozszerzenia przeglądarki i wybrane smartwatche [8].
- **Ocena UX — interpretacja:** połączenie listy i planera dziennego jest zbieżne z orientacją TaskFlow na dzień; osobne plany Personal, Family i Teams tworzą czytelne kategorie wartości. Jednocześnie różne produktywnościowe obszary mogą poszerzać nawigację. Nie jest to wynik testu.
- **Potencjalna bariera — interpretacja:** różnice funkcji między planami i platformami mogą wymagać od użytkownika sprawdzenia, gdzie dana funkcja jest dostępna.

## 6. Feature Comparison Matrix

**Legenda:** ✓ funkcja potwierdzona w źródłach; ◐ częściowa, zależna od planu/platformy lub opisana warunkowo; — niepotwierdzona w źródłach użytych w tej analizie. „—” nie oznacza, że produkt na pewno jej nie ma.

| Funkcja | Todoist | Microsoft To Do | TickTick | Google Tasks | Any.do |
|---|:---:|:---:|:---:|:---:|:---:|
| Bezpłatny plan / dostęp | ✓ [1] | ✓ [13] | ✓ [6] | ✓ [4] | ✓ [7] |
| Szybkie dodawanie / wejście naturalnym językiem | ✓ [10] | ◐ [9] | ✓ [3] | ◐ [17] | ◐ [8] |
| Zadania na dziś / planner dnia | ✓ [1] | ✓ [9] | ✓ [3] | ◐ [4] | ✓ [7] |
| Priorytety | ✓ [1] | ✓ [9] | ✓ [3] | ✓ [4] | ◐ [8] |
| Terminy i przypomnienia | ✓ [1, 2] | ✓ [9] | ✓ [3, 6] | ✓ [4, 17] | ✓ [7, 8] |
| Zadania cykliczne | ✓ [2] | ◐ [9] | ✓ [3] | ✓ [17] | ◐ [7, 8] |
| Podzadania / kroki | ✓ [2] | ✓ [9] | ✓ [3] | ✓ [4, 17] | ✓ [8] |
| Wiele list / kategorie | ✓ [1, 2] | ✓ [9] | ✓ [3, 6] | ✓ [4] | ✓ [7, 8] |
| Widok kalendarza | ◐ [1, 2] | ◐ [9] | ◐ [3, 6] | ◐ [4] | ◐ [7, 8] |
| Tablica Kanban | ✓ [1] | — | ✓ [3, 6] | — | ◐ [7] |
| Współdzielenie / współpraca | ✓ [2] | ✓ [14] | ✓ [3, 6] | ◐ [4] | ✓ [7, 8] |
| Synchronizacja między urządzeniami | ✓ [12] | ✓ [15] | ✓ [6, 16] | ✓ [4, 5] | ✓ [8] |
| Platformy web + mobile | ✓ [12] | ✓ [15] | ✓ [16] | ✓ [4, 5] | ✓ [8] |
| Desktopowe aplikacje | ✓ [12] | ✓ [15] | ✓ [16] | ◐ [4] | ✓ [8] |
| Funkcje skupienia / habit tracker | — | — | ✓ [3] | — | ◐ [7, 8] |

**Uwagi do macierzy:** wpisy odzwierciedlają zakres potwierdzony w wybranych źródłach producentów na dzień dostępu. Kalendarz i współpraca są szczególnie zależne od konkretnego planu, urządzenia lub integracji. Macierz nie jest wynikiem uruchomienia każdej aplikacji i nie powinna być traktowana jako pełna specyfikacja produktów.

## 7. UX/UI Benchmarking

### 7.1 Kryteria oceny

Skala **1–5**: 1 = słabe dopasowanie do kryterium w analizowanych publicznych materiałach; 3 = poprawne/umiarkowane; 5 = mocne dopasowanie do założenia TaskFlow „proste codzienne zadania”. Wynik jest oceną ekspercką zakresu, architektury funkcji i publicznie opisywanych przepływów, a nie testem z użytkownikami ani oceną jakości kodu.

| Kryterium | Co oceniamy |
|---|---|
| Prostota interfejsu | Czy produkt umożliwia podstawowe użycie bez konieczności konfigurowania wielu pojęć i narzędzi? |
| Czytelność widoku głównego | Czy da się wskazać zadania do wykonania teraz i ich status? |
| Nawigacja | Czy główne obszary i modele organizacji wydają się zrozumiałe na podstawie publicznych opisów? |
| Dodawanie i edycja | Czy dostępna jest krótka ścieżka zapisu/uzupełnienia zadania? |
| Hierarchia wizualna | Czy dostępne są mechanizmy odróżniania priorytetu, terminu i statusu? |
| Accessibility | Czy publiczne materiały potwierdzają konkretne udogodnienia dostępnościowe? Punkty nie zastępują audytu WCAG. |
| Responsywność | Czy produkt deklaruje obsługę web, mobile i/lub desktop, a więc użycie na różnych klasach urządzeń? |

### 7.2 Macierz punktowa

**Bezpośrednie sprawdzenie:** oficjalne cenniki, strony funkcji, dokumentacja pomocy i publiczne przykłady/zrzuty producentów.  
**Nie sprawdzono bezpośrednio:** bieżących aplikacji interaktywnie na wielu urządzeniach, z czytnikiem ekranu, z użytkownikami ani w ramach audytu Accessibility. Wszystkie oceny poniżej są zatem ocenami dokumentacyjnymi/public-materials only.

| Produkt | Prostota | Widok główny | Nawigacja | Dodawanie/edycja | Hierarchia wizualna | Accessibility | Responsywność | Uzasadnienie skrócone |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| Todoist | 3 | 4 | 3 | 5 | 5 | 3 | 5 | Quick Add i priorytety mocne; projekty/sekcje/etykiety/filtry zwiększają elastyczność i liczbę pojęć [1, 2, 10, 12]. Accessibility oceniono neutralnie z powodu braku systematycznego audytu w tym badaniu. |
| Microsoft To Do | 4 | 5 | 4 | 4 | 4 | 3 | 5 | „My Day”, sugestie, listy i kroki tworzą czytelny model dzienny; integracja Outlook/Exchange wzmacnia spójność w ekosystemie Microsoft [5, 9, 14, 15]. |
| TickTick | 2 | 4 | 2 | 5 | 5 | 3 | 5 | Bardzo bogaty zestaw wejść, widoków i narzędzi; to mocna elastyczność, ale największy zakres do nauczenia się w porównaniu [3, 6, 16]. |
| Google Tasks | 5 | 4 | 4 | 4 | 3 | 3 | 4 | Niewielki zestaw podstawowych funkcji i integracja Workspace sprzyjają prostemu użyciu; mniejszy zestaw trybów organizacji ogranicza konfigurację, ale też możliwości [4, 17]. |
| Any.do | 3 | 4 | 3 | 4 | 4 | 3 | 5 | Widok My Day, kalendarz i różne plany łączą zadania osobiste z planowaniem; plan Family/Teams rozszerza produkt poza prostą listę [7, 8]. |

**Jak czytać wynik Accessibility:** wartość 3 nie oznacza zgodności ani jej braku. W tej analizie nie wykonywano audytu klawiatury, kontrastu, powiększenia, semantyki czytnika ekranu ani WCAG. Punktacja jest neutralna, gdy źródła nie pozwalają uzasadnić mocniejszego wniosku.

### 7.3 Wnioski benchmarkingowe

- Szybkie dodawanie jest obszarem, w którym konkurenci ustawili wysoką poprzeczkę. TaskFlow powinien umożliwiać zapis samego tytułu jednym krótkim przepływem.
- Widok „Dzisiaj” nie jest sam w sobie wyróżnikiem. Jego jakość będzie zależeć od czytelności statusów, zaległych zadań i prostego przesuwania planu.
- Nie należy kopiować pełnej liczby widoków TickTick. MVP może zacząć od listy i sekcji „Dzisiaj / Zaległe / Później”.
- Dostępność należy potraktować jako wymaganie projektowe, a nie punkt w tabeli marketingowej: fokus klawiatury, obsługa bez przeciągania, kontrast, etykiety i odpowiedni rozmiar kontrolek [11].
- Responsywność wymaga odrębnych układów dla telefonu i dużego ekranu; samo zmniejszenie desktopowej listy nie gwarantuje czytelnego mobilnego przepływu.

## 8. SWOT Analysis

| Strengths — mocne strony | Weaknesses — słabe strony |
|---|---|
| Jasny, ograniczony problem: codzienne zadania, szybkie dodanie, przegląd i ukończenie. | Projekt koncepcyjny — brak działającego produktu, użytkowników, telemetrii i dowodu retencji. |
| Spójny kierunek z User Research: widok „Dzisiaj”, widoczne priorytety, czytelne zaległe zadania i spokojny interfejs. | Syntetyczne odpowiedzi w dotychczasowym User Research nie dowodzą, że problem występuje w tej skali lub u wybranej grupy. |
| MVP może być małe i możliwe do prototypowania oraz walidacji w Figma. | Funkcje podstawowe są już dostępne bezpłatnie w Google Tasks i Microsoft To Do, a także w darmowych planach konkurentów freemium. |
| Projekt może wykazać pełny tok pracy BA/UX: brief, hipotezy, przepływ, prototyp i walidację. | Brak jeszcze potwierdzonej segmentacji użytkowników, przewagi produktowej, architektury synchronizacji i modelu biznesowego. |

| Opportunities — szanse | Threats — zagrożenia |
|---|---|
| Walidacja segmentu, który chce listy dnia bez rozbudowanej konfiguracji. | Wysokie oczekiwania względem synchronizacji, przypomnień i dostępności na wielu platformach. |
| Uproszczenie „capture → plan → complete” oraz łatwe odróżnianie zadań zaległych. | Silne ekosystemy Google i Microsoft mogą mieć przewagę integracji i dystrybucji. |
| Dostępność jako cecha jakości: kontrast, obsługa klawiaturą, proste cele dotykowe, jasny język. | Rozrost zakresu funkcji może rozmyć podstawową obietnicę „prostej listy dnia”. |
| Testy prototypu mogą szybko obalić lub potwierdzić kluczowe założenia przed implementacją. | Bezpieczeństwo danych i niezawodność powiadomień/synchronizacji stają się istotnymi wymaganiami, jeżeli projekt przejdzie do realnego produktu. |

## 9. MVP Recommendations — MoSCoW

Priorytety odnoszą się do minimalnego prototypu/produktu do walidacji głównego przepływu, a nie pełnego systemu produkcyjnego.

### Must have

- Dodanie zadania przez pojedyncze pole tytułu i widoczny przycisk „Dodaj”.
- Edycja i usuwanie zadania z prostym, przewidywalnym potwierdzeniem dla działań destrukcyjnych.
- Główny widok „Dzisiaj” z czytelnym stanem pustym.
- Jednoznaczne oznaczenie zadania jako wykonanego z poziomu listy.
- Statusy lub sekcje „Dzisiaj”, „Zaległe” i „Później” albo równoważny prosty sposób odróżnienia terminu.
- Podstawowy priorytet (np. ważne / standardowe) widoczny także bez rozróżnienia samym kolorem.
- Responsywny układ mobile-first oraz obsługa klawiatury dla głównych czynności.
- Kontrast, widoczny fokus, etykiety kontrolek i rozmiary celów zgodne z przyjętym celem WCAG 2.2 AA [11].

### Should have

- Termin oraz opcjonalne przypomnienie dla zadania.
- Powtarzanie zadania z kilkoma prostymi presetami (np. codziennie/tygodniowo).
- Podzadania dla rozbicia większego zadania.
- Edycja priorytetu i terminu bez opuszczania głównego kontekstu.
- Proste filtrowanie lub wyszukiwanie po tytule/sekcji.
- Zapis/synchronizacja między urządzeniami, jeśli zakres projektu przechodzi poza lokalny prototyp.

### Could have

- Widok tygodniowy lub kalendarzowy.
- Kategorie/etykiety tworzone przez użytkownika.
- Skróty klawiaturowe i widget.
- Codzienne podsumowanie postępu.
- Synchronizacja z zewnętrznym kalendarzem.
- Opcjonalny tryb ciemny.

### Won’t have — na tym etapie

- Współpraca zespołowa, role, przypisywanie zadań i komentarze.
- Habit tracker, Pomodoro, macierz Eisenhowera, statystyki produktywności.
- Asystent AI, automatyzacje, generowanie planu dnia i wejście głosowe.
- Rozbudowane dashboardy, wiele typów widoków i zaawansowany język zapytań filtrów.
- Monetyzacja/subskrypcja bez sprawdzenia kosztów, popytu i gotowości do zapłaty.

## 10. Conclusions

### Najważniejsze wnioski

1. **Podstawowy zestaw funkcji jest kategorią oczekiwaną, nie wystarczającym wyróżnikiem.** Szybkie dodawanie, widoki dzienne, priorytety, terminy, przypomnienia i synchronizacja występują u analizowanych konkurentów.
2. **TaskFlow powinien konkurować spójnością przepływu i ograniczeniem zbędnych decyzji.** Ekran główny ma odpowiadać na pytanie „co mam teraz zrobić?”, a dodatkowe ustawienia powinny być dostępne dopiero w razie potrzeby.
3. **Minimalizm wymaga decyzji produktowych.** Samo ograniczenie liczby elementów nie pomaga, jeżeli zaległe zadania, priorytety i ukończenie pozostają nieczytelne.
4. **Dostępność i responsywność trzeba walidować na prototypie.** Zrzuty ekranu nie potwierdzają zgodności z WCAG ani jakości działania na urządzeniach.
5. **Obecne profile uczestników są syntetyczne.** Mogą pomóc przygotować hipotezy i scenariusze testowe, ale nie wolno na ich podstawie pisać, że „użytkownicy potwierdzili” potrzeby.

### Rekomendacje do Figma

- Zbudować jedną główną ścieżkę: dodaj zadanie → zobacz je na liście → oznacz jako wykonane.
- Pokazać trzy stany listy: pusta, z zadaniami dzisiejszymi, z zadaniem zaległym.
- Rozróżnić wizualnie priorytet, termin i status; nie kodować znaczenia wyłącznie kolorem.
- Ograniczyć ekran startowy do listy, szybkiego dodawania oraz jasnych sekcji. Ustawienia dodatkowe przenieść do szczegółów zadania lub ekranu ustawień.
- Przygotować wariant mobilny i desktopowy oraz sprawdzić zawijanie długich nazw i obsługę dużego tekstu.
- Dodać stany fokus/hover/disabled, komunikaty błędów, potwierdzenie usunięcia i informację po zapisaniu.
- Sprawdzić prototyp z rzeczywistymi uczestnikami: poprosić o dodanie zadania z terminem, znalezienie zaległego i ukończenie zadania bez podpowiadania nazw przycisków.

### Ryzyka i założenia wymagające walidacji

| Hipoteza | Ryzyko, jeśli jest fałszywa | Sposób walidacji |
|---|---|---|
| Użytkownik chce zaczynać od listy „Dzisiaj”. | Ekran startowy nie odpowie na główny cel albo będzie ukrywać ważniejsze zadania. | Moderowane testy prototypu i pytanie o naturalny punkt startu. |
| Szybkie dodanie bez wielu pól wystarcza na początku. | Użytkownicy mogą potrzebować terminu/kontekstu już przy zapisie. | Obserwacja zadań, które badani próbują dodać, oraz momentów, w których wracają do edycji. |
| Sekcje „Zaległe / Dzisiaj / Później” są zrozumiałe. | Niejasne statusy mogą prowadzić do gubienia lub błędnego odkładania zadań. | Test sortowania i interpretacji statusów bez instrukcji. |
| Prosty priorytet jest wystarczający. | Użytkownicy mogą potrzebować bardziej rozbudowanego planowania. | Wywiady o rzeczywistych decyzjach „co najpierw” i test kilku wariantów. |
| Użytkownicy zaakceptują ograniczenie widoków w MVP. | Brak kalendarza lub etykiet może uniemożliwić użycie w wybranym segmencie. | Rekrutacja użytkowników o różnym sposobie planowania i test zadań z konkretnymi datami. |
| Polska wersja, synchronizacja i przypomnienia są wystarczające. | Brak platformy lub zawodne powiadomienia szybko obniżą użyteczność. | Testy na docelowych urządzeniach oraz sprawdzenie oczekiwań integracyjnych. |

## 11. Sources & References

**Data dostępu do poniższych stron: 8 listopada 2026 r.** Ceny i limity są zmienne; podano je tak, jak widniały w źródle w dniu dostępu, bez przeliczania na PLN.

1. Todoist, [Pricing](https://www.todoist.com/pricing/) — plany Beginner/Pro/Business, widoki i funkcje.
2. Todoist, [Plans, pricing, and billing FAQ](https://www.todoist.com/pl/help/todoist/billing/todoist-plans-pricing-and-billing-faq-Vq2z0HWL6) — limity planów, kalendarz, przypomnienia i ceny opisane przez producenta.
3. TickTick, [Features](https://www.ticktick.com/features) — Quick Add, organizacja, widoki, przypomnienia i narzędzia produktywności.
4. Google Tasks Help, [Learn about Google Tasks](https://support.google.com/tasks/answer/7675772?hl=en) — zadania w Google Workspace, synchronizacja, szczegóły i podzadania.
5. Google Workspace, [Organize & Track To-Dos with Google Tasks](https://workspace.google.com/intl/en/products/tasks/) — integracje, zadania cykliczne, kalendarz, priorytety i synchronizacja.
6. TickTick, [Upgrade](https://www.ticktick.com/upgrade) — limity Free i Premium oraz cena Premium.
7. Any.do, [Pricing](https://www.any.do/pricing) — plany Personal, Premium, Family i Teams.
8. Any.do Help Center, [Getting Started with Any.do](https://support.any.do/en/articles/8609629-getting-started-with-any-do) oraz [Platforms & Devices](https://support.any.do/en/articles/8609757-platforms-devices) — funkcje i platformy.
9. Microsoft Support, [Welcome to Microsoft To Do](https://support.microsoft.com/en-us/todo/welcome-to-microsoft-to-do) oraz [Plan and connect with Microsoft To Do](https://support.microsoft.com/en-us/todo/plan-and-connect-with-microsoft-to-do) — listy, My Day, sugestie, kroki, terminy i Outlook.
10. Todoist Help Center, [Use Task Quick Add in Todoist](https://www.todoist.com/help/todoist/features/use-task-quick-add-in-todoist-va4Lhpzz) — składnia szybkiego dodawania.
11. W3C, [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/) — standard odniesienia dla kryteriów dostępności.
12. Todoist, [Downloads](https://www.todoist.com/pl/downloads) — obsługiwane platformy i integracje.
13. Microsoft Support, [Which accounts can I use Microsoft To Do with?](https://support.microsoft.com/pl-pl/outlook/which-accounts-can-i-use-microsoft-to-do-with) — bezpłatny dostęp przez konto osobiste oraz warunki dla kont służbowych.
14. Microsoft Support, [Create and share lists](https://support.microsoft.com/en-us/todo/create-and-share-lists) — scenariusze współdzielenia.
15. Microsoft Support, [Set up Microsoft To Do](https://support.microsoft.com/pl-pl/todo/set-up-microsoft-to-do) — dostępność web, Windows, Mac, iOS i Android oraz integracja z Outlook Tasks.
16. TickTick, [Download](https://ticktick.com/download?language=en_US) — platformy aplikacji.
17. Google Tasks Help, [Add or edit a task — Android](https://support.google.com/tasks/answer/7675838?co=GENIE.Platform%3DAndroid&hl=en) — kroki dodawania, termin, powtarzanie, podzadania i powiadomienia.
18. TaskFlow, [02_User_Research.md](./02_User_Research.md) — brief i syntetyczne profile badawcze projektu; użyte wyłącznie jako kontekst projektowy, nie jako źródło danych rynkowych.

---

**Nota portfolio:** niniejszy dokument syntetyzuje publicznie dostępne materiały producentów i standard W3C. Oceny UX są eksperckimi hipotezami opartymi na desk research. Nie były przeprowadzone testy konkurencyjnych aplikacji ani reprezentatywne badanie rynku.
