---
navigation:
  - function.grapheme-stripos.md: « grapheme\_stripos
  - function.grapheme-strlen.md: grapheme\_strlen »
  - index.md: PHP Manual
  - ref.intl.grapheme.md: Функції Grapheme
title: grapheme\_stristr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# grapheme\_stristr

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

grapheme\_stristr — Повертає частину рядка haystack від першої появи needle без урахування регістру до кінця haystack

### Опис

Процедурний стиль

```methodsynopsis
grapheme_stristr(string $haystack, string $needle, bool $beforeNeedle = false): string|false
```

Повертає частину рядка `haystack` від першої появи needle без урахування регістру до кінця `haystack`

### Список параметрів

`haystack`

Вхідний рядок. Має бути коректним UTF-8.

`needle`

Рядок, який потрібно знайти. Має бути коректним UTF-8.

`beforeNeedle`

Якщо **`true`**, функция**grapheme\_stristr()** повертає частину `haystack`до первого появления`needle` (виключаючи `needle`

### Значення, що повертаються

Повертає частину рядка або **`false`**, якщо входження `needle`не найдено.

### Приклади

**Пример #1 Пример использования функции**grapheme\_stristr()\*\*\*\*

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"
$char_O_diaeresis_nfd = "O\xCC\x88"; // 'LATIN CAPITAL LETTER O WITH DIAERESIS' (U+00D6) normalization form "D"

print urlencode(grapheme_stristr( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_a_ring_nfd, $char_O_diaeresis_nfd));

?>
```

Результат виконання наведеного прикладу:

```
o%CC%88a%CC%8A
```

### Дивіться також

-   [grapheme\_stripos()](function.grapheme-stripos.md) \- Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру
-   [grapheme\_strpos()](function.grapheme-strpos.md) \- знаходить позицію (в одиницях графеми) першого входження рядка
-   [grapheme\_strripos()](function.grapheme-strripos.md) \- Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру
-   [grapheme\_strrpos()](function.grapheme-strrpos.md) \- знаходить позицію (в одиницях графеми) останнього входження рядка
-   [grapheme\_strstr()](function.grapheme-strstr.md) \- Повертає частину рядка haystack від першої появи needle до кінця haystack
-   « [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries) »
