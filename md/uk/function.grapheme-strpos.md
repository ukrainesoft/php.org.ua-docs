---
navigation:
  - function.grapheme-strlen.md: « grapheme\_strlen
  - function.grapheme-strripos.md: grapheme\_strripos »
  - index.md: PHP Manual
  - ref.intl.grapheme.md: Функції Grapheme
title: grapheme\_strpos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# grapheme\_strpos

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

grapheme\_strpos - Знаходить позицію (в одиницях графеми) першого входження рядка

### Опис

Процедурний стиль

```methodsynopsis
grapheme_strpos(string $haystack, string $needle, int $offset = 0): int|false
```

Знаходить позицію (в одиницях графеми) першого входження рядка.

### Список параметрів

`haystack`

Рядок для пошуку. Має бути коректним UTF-8.

`needle`

Рядок, який потрібно знайти. Має бути коректним UTF-8.

`offset`

Необов'язковий параметр `offset` дозволяє вказати, де в `haystack` починати пошук у вигляді усунення в одиницях графеми (не в байтах чи символах). Якщо усунення негативне, воно обробляється щодо кінця рядка. Повернена позиція, як і раніше, щодо початку `haystack`, независимо от значения`offset`

### Значення, що повертаються

Повертає позицію як ціле число. Якщо входження `needle`не найдено, функция**grapheme\_strpos()** поверне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Додано підтримку негативних значень `offset` |

### Приклади

**Приклад #1 Приклад використання** grapheme\_strpos()\*\*\*\*

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print grapheme_strpos( $char_a_ring_nfd . $char_a_ring_nfd . $char_o_diaeresis_nfd, $char_o_diaeresis_nfd);

?>
```

Результат виконання наведеного прикладу:

```
2
```

### Дивіться також

-   [grapheme\_stripos()](function.grapheme-stripos.md) \- Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру
-   [grapheme\_stristr()](function.grapheme-stristr.md) \- Повертає частину рядка haystack від першої появи needle без урахування регістру до кінця haystack
-   [grapheme\_strripos()](function.grapheme-strripos.md) \- Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру
-   [grapheme\_strrpos()](function.grapheme-strrpos.md) \- знаходить позицію (в одиницях графеми) останнього входження рядка
-   [grapheme\_strstr()](function.grapheme-strstr.md) \- Повертає частину рядка haystack від першої появи needle до кінця haystack
-   [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)
