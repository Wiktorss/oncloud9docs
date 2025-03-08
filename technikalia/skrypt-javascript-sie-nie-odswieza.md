---
icon: js
description: >-
  Ta Knowledge Base zawiera szczegółowe instrukcje, jak rozwiązać problem z
  JavaScriptem, który nie odświeża się poprawnie przez cache oraz nasz algorytm
  w litespeed.
---

# Skrypt JavaScript się nie odświeża

Link do udostępnienia tego artykułu: [Skrypt JavaScript się nie odświeża](https://oncloud9.gitbook.io/docs/technikalia/skrypt-javascript-sie-nie-odswieza)

**Skrypt JavaScript się nie odświeża? Oto szybka naprawa!**

Masz wrażenie, że Twój JavaScript nie odświeża się po wprowadzeniu zmian? Spokojnie, oto jak to ogarnąć w kilku prostych krokach. 😎

#### 1. **Dodaj atrybut `data-no-optimize`**

Jeśli korzystasz z LiteSpeed Cache, możesz szybko wykluczyć skrypt z optymalizacji, dodając atrybut `data-no-optimize` w kodzie HTML:

```
<script src="script.js" data-no-optimize="1"></script>
```

Dzięki temu LiteSpeed Cache zignoruje wskazane skrypty.

#### 2. **Sprawdź przeglądarkę**

Przeglądarki lubią keszować pliki JavaScript, więc najpierw:

* Użyj skrótu klawiszowego **Ctrl + F5** (lub **Cmd + Shift + R** na Macu), aby wymusić odświeżenie z pominięciem kesza.
* Jeśli to nie pomoże, wyczyść kesz przeglądarki w ustawieniach.

#### 3. **Dodaj parametr wersji**

Dodaj parametr wersji do swojego pliku JS. W pliku HTML zmień:

```
<script src="script.js"></script>
```

na:

```
<script src="script.js?v=1.0"></script>
```

Zmiana wersji (np. na **v=1.1**) wymusi ładowanie nowego pliku.

#### 4. **LiteSpeed Cache – Wyklucz pliki JS**

Jeśli atrybut `data-no-optimize` nie wystarczy, możesz użyć filtra w WordPressie, aby wykluczyć wybrane pliki JavaScript z optymalizacji:

<pre><code>add_filter('litespeed_optimize_js_excludes', function($excludes) {
<strong>    $excludes[] = '/ścieżka/do/skryptu.js';
</strong>    return $excludes;
});
</code></pre>

#### 5. **Sprawdź błędy w konsoli**

Otwórz konsolę deweloperską (F12 w przeglądarce) i sprawdź, czy nie pojawiają się żadne błędy JavaScript.

Jeśli żaden z powyższych sposobów nie działa, daj znać naszemu wsparciu technicznemu na [onCloud9.io](https://oncloud9.io/), w szczególności jeśli AI nie może pomóc, to poproś o kontakt z człowiekiem. Chętnie pomożemy! 💡
