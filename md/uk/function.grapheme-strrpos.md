---
navigation:
  - function.grapheme-strripos.md: « graphemestrripos
  - function.grapheme-strstr.md: graphemestrstr »
  - index.md: PHP Manual
  - ref.intl.grapheme.md: Функции Grapheme
title: graphemestrrpos
---
# graphemestrrpos

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

graphemestrrpos - Знаходить позицію (в одиницях графеми) останнього входження рядка

### Опис

Процедурний стиль

```methodsynopsis
grapheme_strrpos(string $haystack, string $needle, int $offset = 0): int|false
```

Знаходить позицію (в одиницях графеми) останнього входження рядка.

### Список параметрів

`haystack`

Рядок для пошуку. Має бути коректним UTF-8.

`needle`

Рядок, який потрібно знайти. Має бути коректним UTF-8.

`offset`

Необов'язковий параметр `offset` дозволяє вказати, де в `haystack` починати пошук у вигляді усунення в одиницях графеми (не в байтах чи символах). Якщо усунення негативне, воно обробляється щодо кінця рядка. Повернена позиція, як і раніше, щодо початку `haystack`незалежно від значення `offset`

### Значення, що повертаються

Повертає позицію як ціле число. Якщо входження `needle` не знайдено, функція **graphemestrrpos()** поверне **`false`**

### Приклади

**Приклад #1 Приклад використання **graphemestrrpos()****

```php
<?php
$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print grapheme_strrpos( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_o_diaeresis_nfd, $char_o_diaeresis_nfd);
?>
```

Результат виконання цього прикладу:

```
2
```

### Дивіться також

-   [graphemestripos()](function.grapheme-stripos.md) - Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру
-   [graphemestristr()](function.grapheme-stristr.md) - Повертає частину рядка haystack від першої появи needle без урахування регістру до кінця haystack
-   [graphemestrpos()](function.grapheme-strpos.md) - знаходить позицію (в одиницях графеми) першого входження рядка
-   [graphemestrripos()](function.grapheme-strripos.md) - Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру
-   [graphemestrstr()](function.grapheme-strstr.md) - Повертає частину рядка haystack від першої появи needle до кінця haystack
-   [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)
