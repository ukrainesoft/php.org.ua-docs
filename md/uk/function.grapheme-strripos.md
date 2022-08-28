Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру

-   [« grapheme\_strpos](function.grapheme-strpos.html)
    
-   [grapheme\_strrpos »](function.grapheme-strrpos.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Grapheme](ref.intl.grapheme.html)
    
-   Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру
    

# graphemestrripos

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

graphemestrripos - Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру

### Опис

Процедурний стиль

```methodsynopsis
grapheme_strripos(string $haystack, string $needle, int $offset = 0): int|false
```

Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру.

### Список параметрів

`haystack`

Рядок для пошуку. Має бути коректним UTF-8.

`needle`

Рядок, який потрібно знайти. Має бути коректним UTF-8.

`offset`

Необов'язковий параметр `offset` дозволяє вказати, де в `haystack` починати пошук у вигляді усунення в одиницях графеми (не в байтах чи символах). Якщо усунення негативне, воно обробляється щодо кінця рядка. Повернена позиція, як і раніше, щодо початку `haystack`незалежно від значення `offset`

### Значення, що повертаються

Повертає позицію як ціле число. Якщо входження `needle` не знайдено, функція **graphemestrripos()** поверне **`false`**

### Приклади

**Приклад #1 Приклад використання **graphemestrripos()****

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"
$char_O_diaeresis_nfd = "O\xCC\x88"; // 'LATIN CAPITAL LETTER O WITH DIAERESIS' (U+00D6) normalization form "D"

print grapheme_strripos( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_o_diaeresis_nfd, $char_O_diaeresis_nfd);

?>
```

Результат виконання цього прикладу:

```
2
```

### Дивіться також

-   [grapheme\_stripos()](function.grapheme-stripos.html) - Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру
-   [grapheme\_stristr()](function.grapheme-stristr.html) - Повертає частину рядка haystack від першої появи needle без урахування регістру до кінця haystack
-   [grapheme\_strpos()](function.grapheme-strpos.html) - знаходить позицію (в одиницях графеми) першого входження рядка
-   [grapheme\_strrpos()](function.grapheme-strrpos.html) - знаходить позицію (в одиницях графеми) останнього входження рядка
-   [grapheme\_strstr()](function.grapheme-strstr.html) - Повертає частину рядка haystack від першої появи needle до кінця haystack
-   [»  Сегментация текста в Unicode: границы кластера графемы](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)