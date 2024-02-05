---
navigation:
  - function.grapheme-extract.md: « grapheme\_extract
  - function.grapheme-stristr.md: grapheme\_stristr »
  - index.md: PHP Manual
  - ref.intl.grapheme.md: Функції Grapheme
title: grapheme\_stripos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# grapheme\_stripos

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

grapheme\_stripos — Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру

### Опис

Процедурний стиль

```methodsynopsis
grapheme_stripos(string $haystack, string $needle, int $offset = 0): int|false
```

Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру.

### Список параметрів

`haystack`

Рядок для пошуку. Має бути коректним UTF-8.

`needle`

Рядок, який потрібно знайти. Має бути коректним UTF-8.

`offset`

Необов'язковий параметр `offset` дозволяє вказати, де в `haystack` починати пошук у вигляді усунення в одиницях графеми (не в байтах чи символах). Якщо усунення негативне, воно обробляється щодо кінця рядка. Повернена позиція, як і раніше, щодо початку `haystack`, независимо от значения`offset`

### Значення, що повертаються

Повертає позицію як ціле число. Якщо входження `needle`не найдено, функция**grapheme\_stripos()** поверне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Додано підтримку негативних значень `offset` |

### Приклади

**Пример #1 Пример использования**grapheme\_stripos()\*\*\*\*

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"
$char_O_diaeresis_nfd = "O\xCC\x88"; // 'LATIN CAPITAL LETTER O WITH DIAERESIS' (U+00D6) normalization form "D"

print grapheme_stripos( $char_a_ring_nfd . $char_a_ring_nfd . $char_o_diaeresis_nfd, $char_O_diaeresis_nfd);

?>
```

Результат виконання наведеного прикладу:

```
2
```

### Дивіться також

-   [grapheme\_stristr()](function.grapheme-stristr.md) \- Повертає частину рядка haystack від першої появи needle без урахування регістру до кінця haystack
-   [grapheme\_strpos()](function.grapheme-strpos.md) \- знаходить позицію (в одиницях графеми) першого входження рядка
-   [grapheme\_strripos()](function.grapheme-strripos.md) \- Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру
-   [grapheme\_strrpos()](function.grapheme-strrpos.md) \- знаходить позицію (в одиницях графеми) останнього входження рядка
-   [grapheme\_strstr()](function.grapheme-strstr.md) \- Повертає частину рядка haystack від першої появи needle до кінця haystack
-   [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)
