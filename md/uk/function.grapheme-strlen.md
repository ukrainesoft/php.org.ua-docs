---
navigation:
  - function.grapheme-stristr.md: « graphemestristr
  - function.grapheme-strpos.md: graphemestrpos »
  - index.md: PHP Manual
  - ref.intl.grapheme.md: Функции Grapheme
title: graphemestrlen
---
# graphemestrlen

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

graphemestrlen — Отримує довжину рядка в одиницях графеми

### Опис

Процедурний стиль

```methodsynopsis
grapheme_strlen(string $string): int|false|null
```

Отримує довжину рядка в одиницях графеми (не байти чи символи)

### Список параметрів

`string`

Рядок, який необхідно виміряти. Повинний бути коректний рядок кодування UTF-8.

### Значення, що повертаються

Довжина рядка у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **graphemestrlen()****

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print grapheme_strlen( 'abc' . $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_a_ring_nfd);

?>
```

Результат виконання цього прикладу:

```
6
```

### Дивіться також

-   [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)
-   [iconvstrlen()](function.iconv-strlen.md) - Повертає кількість символів у рядку
-   [мбstrlen()](function.mb-strlen.md) - Отримує довжину рядка
-   [strlen()](function.strlen.md) - Повертає довжину рядка
