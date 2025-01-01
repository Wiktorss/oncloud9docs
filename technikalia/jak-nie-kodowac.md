---
description: >-
  Ta Knowledge Base zawiera wskazówki, jak unikać błędów kodowania w WordPress,
  które mogą spowolnić działanie strony. Dowiesz się, jak zoptymalizować
  skrypty, obrazy i wtyczki, aby zwiększyć wydajność.
icon: democrat
---

# Jak NIE kodować

Link do udostępnienia tego artykułu: [Jak NIE kodować](jak-nie-kodowac.md)

## Jak NIE kodować w WordPressie?

Kodowanie w WordPressie to sztuka, ale pamiętaj o wydajności – inaczej Twoja strona stanie się bramą do piekła powolności. Nasze skrypty działają jak dobrze naoliwiona maszyna, ale jeśli popełnisz błędy, nawet najlepszy algorytm Ci nie pomoże! Oto lista rzeczy, których warto unikać, aby Twoja strona nie zamulała.

### 1. **RODO nie znaczy „Raz Ominąć, Dalej Obojętne"**

Pamiętaj, użytkownicy to nie króliki doświadczalne – nie będą tolerować ładowania ton skryptów przed kliknięciem „Akceptuję". Tak, mówimy o RODO! Niektórzy ładują wszystkie trackery, zanim użytkownik wyrazi zgodę na cookies. To tylko wydłuża czas ładowania strony, bo ciągniesz skrypty bez czekania na zgodę.

Wstrzymaj te skrypty do momentu zgody użytkownika – zobaczysz, jak Twoja strona przyspieszy. Dobrze skonfigurowany mechanizm zgody na cookies nie tylko spełnia wymogi prawne, ale także poprawia wydajność. Ładowanie trackerów po akceptacji da Twojej stronie prawdziwego „powera".

### 2. **Obrazy – Albo Zoptymalizowane, Albo Wcale!**

**Po co instalować kolejny „mega-skomplikowany" plugin do optymalizacji obrazów, skoro my już to zrobiliśmy za Ciebie?** Nasz algorytm optymalizuje obrazki, by ważyły mniej i nie psuły wydajności strony. Jeśli planujesz instalować plugin do tego celu, przemyśl to – lepiej od razu wykreśl go z listy.

I jeszcze jedno – nieistniejące zdjęcia tylko zwiększają czas ładowania. Odwołanie do nieistniejącego obrazu to +1 sekunda na starcie. A +1s w tym przypadku to jak postój w korku, tylko że na Twojej stronie.

### 3. **Nie Wszystko Wymaga Wtyczki!**

Tak, wiem, kochasz wtyczki. I choć nie mamy nic przeciwko, warto zwrócić uwagę na pewną rzecz. Wiele wtyczek, zwłaszcza tych związanych z elementami strony, ma wbudowane ustawienia wydajności. To nie magia – to funkcjonalność, którą wystarczy włączyć, by Twoja strona działała lepiej.

Zanim odejdziesz od komputera, sprawdź, czy nie masz już opcji optymalizacji w zainstalowanych wtyczkach. One nie gryzą, a jeśli Cię „ugryzą", zawsze możesz je wyłączyć. Warto dać im szansę.

### 4. **JavaScript – Czas na Vanilla JS!**

Słuchaj, to już nie 2015 rok, żeby wciskać jQuery wszędzie, jakby to był jedyny sposób programowania. Nie, nie i jeszcze raz nie. Mimo że WordPress ładuje jQuery domyślnie, nie oznacza to, że musisz go używać do wszystkiego. Każdy dodatkowy skrypt JS to dodatkowe obciążenie strony.

Jeśli musisz coś dodać, używaj _vanilla JS_ (czysty JS) – działa szybciej i nie wymaga ładowania całej biblioteki jQuery. W przeciwnym razie strona będzie czekać na załadowanie jQuery, a Ty stracisz cenne sekundy. Twój użytkownik nie będzie czekał na wymówki – od razu kliknie „Zamknij", gdy strona nie załaduje się w 2 sekundy.

### 5. **Zbędne Skrypty, Zbędne Problemy**

Zanim dodasz jakikolwiek skrypt, zadaj sobie jedno pytanie: „Czy to naprawdę potrzebne?" Niepotrzebne skrypty tylko przyspieszają drogę Twojej strony do piekła powolności. Pamiętaj, im więcej elementów do załadowania, tym wolniejsza strona.

Daj sobie czas na przemyślenie, co jest absolutnie konieczne, a co to tylko dodatkowe obciążenie. Jeśli coś jest „tylko dla efektu", ale nie ma realnego wpływu na funkcjonalność, po prostu to usuń. Oszczędzisz czas ładowania.
