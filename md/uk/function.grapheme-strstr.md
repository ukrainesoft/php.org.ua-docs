---
navigation:
  - function.grapheme-strrpos.html: « graphemestrrpos
  - function.grapheme-substr.html: graphemesubstr »
  - index.html: PHP Manual
  - ref.intl.grapheme.html: Функции Grapheme
title: graphemestrstr
---
# graphemestrstr

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

graphemestrstr - Повертає частину рядка haystack від першої появи needle до кінця haystack

### Опис

Процедурний стиль

```methodsynopsis
grapheme_strstr(string $haystack, string $needle, bool $beforeNeedle = false): string|false
```

Повертає частину рядка haystack від першої появи needle до кінця haystack (включаючи needle).

### Список параметрів

`haystack`

Вхідний рядок. Має бути коректним UTF-8.

`needle`

Рядок, який потрібно знайти. Має бути коректним UTF-8.

`beforeNeedle`

Якщо **`true`**, функція **graphemestrstr()** повертає частину `haystack` перед першою появою `needle` (виключаючи `needle`

### Значення, що повертаються

Повертає частину рядка `haystack` або **`false`**, якщо входження `needle` не знайдено.

### Приклади

**Приклад #1 Приклад використання **graphemestrstr()****

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print urlencode(grapheme_stristr( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_a_ring_nfd, $char_o_diaeresis_nfd));

?>
```

Результат виконання цього прикладу:

```
o%CC%88a%CC%8A
```

### Дивіться також

-   [graphemestristr()](function.grapheme-stristr.html) - Повертає частину рядка haystack від першої появи needle без урахування регістру до кінця haystack
-   [graphemestripos()](function.grapheme-stripos.html) - Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру
-   [graphemestrpos()](function.grapheme-strpos.html) - знаходить позицію (в одиницях графеми) першого входження рядка
-   [graphemestrripos()](function.grapheme-strripos.html) - Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру
-   [graphemestrrpos()](function.grapheme-strrpos.html) - знаходить позицію (в одиницях графеми) останнього входження рядка
-   [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)
