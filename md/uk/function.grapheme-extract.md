---
navigation:
  - ref.intl.grapheme.md: « Функции Grapheme
  - function.grapheme-stripos.html: graphemestripos »
  - index.md: PHP Manual
  - ref.intl.grapheme.md: Функции Grapheme
title: graphemeextract
---
# graphemeextract

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

graphemeextract — Функція для вилучення послідовності кластерів за замовчуванням графем з текстового буфера, яка повинна бути закодована в UTF-8

### Опис

Процедурний стиль

```methodsynopsis
grapheme_extract(    string $haystack,    int $size,    int $type = GRAPHEME_EXTR_COUNT,    int $offset = 0,    int &$next = null): string|false
```

Функція для вилучення послідовності кластерів за замовчуванням графем з текстового буфера, яка повинна бути закодована в UTF-8.

### Список параметрів

`haystack`

Рядок для пошуку.

`size`

Максимальна кількість елементів, що повертаються на основі `type`

`type`

Визначає тип одиниць, на які вказує параметр `size`

-   GRAPHEMEEXTRCOUNT (за замовчуванням) - `size` - кількість кластерів графеми для вилучення за замовчуванням.
-   GRAPHEMEEXTRMAXBYTES - `size` - максимальна кількість байтів, що повертаються.
-   GRAPHEMEEXTRMAXCHARS - `size` - це максимальна кількість символів UTF-8, що повертаються.

`offset`

Початкова позиція `haystack` в байтах - якщо задано, воно має бути нулем або позитивним значенням, яке менше або дорівнює довжині `haystack` в байтах, або негативним значенням, що відраховується від кінця `haystack`. Якщо `offset` не вказує перший байт символу UTF-8, початкова позиція переміщається на межу наступного символу.

`next`

Посилання на значення, яке буде встановлене для наступної початкової позиції. Коли дзвінок повертається, це може вказувати на позицію першого байта за кінцем рядка.

### Значення, що повертаються

Рядок, що починається зі зміщення `offset` і межа кластера графеми, що закінчується, за замовчуванням, яка відповідає зазначеним `size` і `type` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано підтримку негативних значень `offset` |

### Приклади

**Приклад #1 Приклад використання **graphemeextract()****

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print urlencode(grapheme_extract( $char_a_ring_nfd . $char_o_diaeresis_nfd, 1, GRAPHEME_EXTR_COUNT, 2));

?>
```

Результат виконання цього прикладу:

```
o%CC%88
```

### Дивіться також

-   [graphemesubstr()](function.grapheme-substr.html) - Повертає частину рядка
-   [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)
