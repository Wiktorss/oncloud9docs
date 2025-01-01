---
icon: globe
description: >-
  Ta Knowledge Base zawiera kompletny przewodnik po zarządzaniu domenami, w tym
  parkowanie, zmianę, cesję i transfer domeny. Dowiesz się, jak prawidłowo
  skonfigurować domenę i uniknąć problemów.
---

# Konfiguracja domeny

Link do udostępnienia tego artykułu: [Konfiguracja domeny](https://oncloud9.gitbook.io/docs/technikalia/konfiguracja-domeny)

<mark style="color:red;">**Ważne! Pamiętaj o rekordzie SPF przypisanym do domeny v=spf1 ip4:178.255.46.130 ip4:178.255.46.131 include:mail.oncloud9.io \~all**</mark>

### Kompleksowy przewodnik po zarządzaniu domenami, cesji i transferze domeny

## 1. **Co to jest domena?**

Domena to adres internetowy, który umożliwia odnalezienie Twojej strony w sieci. Posiadanie własnej domeny daje Ci pełną kontrolę nad prezentacją Twojej witryny online. Wybór odpowiedniej domeny stanowi pierwszy krok do sukcesu w internecie, a jej zarządzanie zapewnia swobodę w kształtowaniu wizerunku online.

## 2. **Rodzaje domen**

* **Domena główna** – To podstawowy adres, na który wskazuje Twoja strona internetowa (np. `mojastrona.pl`).
* **Subdomena** – Subdomeny to dodatkowe adresy powiązane z domeną główną, np. `blog.mojastrona.pl` lub `sklep.mojastrona.pl`. Służą do organizacji treści na stronie.
* **Domena tymczasowa** – Domena przypisana do Twojej strony przed zakupem docelowej domeny. Jest przydatna, gdy zaczynasz budować swoją obecność online.

## 3. **Parkowanie domeny**

Parkowanie domeny to przypisanie jej do konta bez używania do aktywnej strony. Często stosuje się je przy zakupie domeny z myślą o późniejszym uruchomieniu lub zabezpieczeniu nazwy przed podjęciem decyzji o jej pełnym wykorzystaniu.

### **Jak działa parkowanie domeny?**

Po zakupie domeny, jeśli nie chcesz jej jeszcze używać, możesz ją „zaparkować" i przypisać do swojego konta hostingowego. Domena będzie zarejestrowana, ale nie będzie wyświetlać aktywnej strony. Zamiast tego możesz ustawić stronę parkingową, informującą, że domena jest w trakcie konfiguracji.

### **Co się stanie, gdy nie opłacisz domeny?**

Jeśli nie opłacisz swojej domeny, po wygaśnięciu okresu ważności strona przestanie się wyświetlać, a domena stanie się niedostępna. Pamiętaj, że domenę można odzyskać, ale wiąże się to z dodatkowymi kosztami.

### 4. **Zmiana domeny**

Czasem decydujesz się na zmianę domeny, nawet jeśli była już wcześniej używana. Zmiana może dotyczyć nazwy lub końcówki (np. z `.com` na `.pl`). Pamiętaj, że nie jest to tak proste, jak zmiana nazwiska na Facebooku. Jeśli zmienisz domenę bez odpowiedniego dostosowania wszystkich ustawień strony, np. plików WordPressa, strona może przestać działać. **Przy zmianie domeny bądź ostrożny i dobrze zaplanuj wszystkie kroki.**

### **Co się dzieje po zmianie domeny?**

* Bez zmiany plików WordPressa zgodnie z nową domeną, Twoja strona może wyświetlać błędy lub przekierowywać użytkowników na nieprawidłowe adresy.
* Linki wewnętrzne i zewnętrzne mogą prowadzić do błędów 404, co negatywnie wpłynie na SEO i doświadczenia użytkowników.
* Strona może przestać działać poprawnie bez aktualizacji wszystkich ustawień związanych z DNS, bazą danych i konfiguracją serwera.

## 5. **Cesja domeny**

Cesja domeny to proces przenoszenia praw do domeny na inną osobę lub firmę, przy czym zmienia się tylko właściciel, a nie sama domena. Jest to często stosowane przy sprzedaży domeny lub przeniesieniu jej na nowego właściciela, np. po zmianie właściciela firmy.

### **Jak działa cesja domeny?**

* **Krok 1: Zgłoszenie zamiaru cesji.** Zgłaszasz zamiar przeniesienia domeny u swojego rejestratora – firmy, która zarejestrowała Twoją domenę.
* **Krok 2: Przekazanie danych.** Podajesz dane kontaktowe nowego właściciela domeny.
* **Krok 3: Weryfikacja.** Rejestrator może poprosić o dodatkową weryfikację tożsamości, np. przesłanie kopii dowodu osobistego.
* **Krok 4: Akceptacja cesji przez nowego właściciela.** Nowy właściciel musi zaakceptować cesję, zazwyczaj poprzez potwierdzenie e-mailem.
* **Krok 5: Finalizacja przeniesienia.** Po zakończeniu formalności domena zostaje przeniesiona na nowego właściciela.

## 6. **Transfer domeny**

Transfer domeny to proces przenoszenia domeny między różnymi rejestratorami (np. z jednej firmy hostingowej do innej). Jeśli chcesz zmienić rejestratora, musisz wykonać transfer domeny.

### **Jak przebiega transfer domeny?**

* **Krok 1: Uzyskanie kodu autoryzacyjnego (EPP).** Do przeprowadzenia transferu potrzebujesz specjalnego kodu autoryzacyjnego, który umożliwi przeniesienie domeny. Znajdziesz go w panelu administracyjnym swojego obecnego rejestratora.
* **Krok 2: Złożenie wniosku o transfer.** Po uzyskaniu kodu złóż wniosek o transfer u nowego rejestratora. Musisz podać kod oraz dane domeny, którą chcesz przenieść.
* **Krok 3: Potwierdzenie transferu.** Po złożeniu wniosku musisz potwierdzić transfer przez e-mail. To kluczowy etap w procesie przenoszenia domeny.
* **Krok 4: Finalizacja transferu.** Po zakończeniu procesu domena zostanie przeniesiona do nowego rejestratora. Od tego momentu będziesz zarządzać nią przez panel nowego rejestratora.

### **Transfer a cesja – czym się różnią?**

* **Cesja domeny** to przeniesienie praw do domeny na innego właściciela, przy czym rejestrator pozostaje ten sam.
* **Transfer domeny** to przeniesienie domeny do innego rejestratora, zmieniając firmę zarządzającą domeną.

## 7. **Podsumowanie**

* **Parkowanie domeny** umożliwia zarejestrowanie domeny i przypisanie jej do konta bez uruchamiania strony.
* **Zmiana domeny** wymaga odpowiedniej konfiguracji plików, by uniknąć problemów.
* **Cesja domeny** to przekazanie praw do domeny innej osobie lub firmie.
* **Transfer domeny** to przeniesienie domeny do innego rejestratora.

Każda z tych opcji ma swoje zastosowanie w różnych sytuacjach – zależnie od tego, czy chcesz sprzedać domenę, przenieść ją do innej firmy, czy zmienić właściciela. Pamiętaj, że niezależnie od wybranej opcji, musisz być świadomy wszystkich kroków, aby uniknąć problemów z dostępnością swojej strony.
