---
navigation:
  - function.grapheme-strstr.md: « grapheme\_strstr
  - ref.intl.idn.md: Функції IDN »
  - index.md: PHP Manual
  - ref.intl.grapheme.md: Функції Grapheme
title: grapheme\_substr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# grapheme\_substr

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

grapheme\_substr — Повертає частину рядка

### Опис

Процедурний стиль

```methodsynopsis
grapheme_substr(string $string, int $offset, ?int $length = null): string|false
```

Повертає частину рядка.

### Список параметрів

`string`

Вхідний рядок. Має бути коректним UTF-8.

`offset`

Початкова позиція в одиницях графеми за промовчанням. Якщо `offset` більше, або дорівнює нулю, рядок, що повертається, буде починатися з позиції `offset` $string, починаючи з нуля. Якщо значення `offset` негативний рядок, що повертається, буде починатися з одиниці графеми `offset`от конца строки.

`length`

Довжина у графемних одиницях. Якщо встановлено позитивне значення `length`, що повертається рядок міститиме не більше `length` одиниць графеми, починаючи зі значення `offset` (залежно від довжини рядка). Якщо встановлено негативне значення `length`, то така кількість одиниць графеми буде опущена в кінці рядка (після того, як початкова позиція була обчислена, якщо параметр `offset` негативний). Якщо `offset` позначає позицію за межами цього усічення, буде повернуто порожній рядок.

### Значення, що повертаються

Повертає витягнуту частину `string`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер послідовно притискає зсуви, що виходять за межі, до кордону рядка. Раніше в деяких випадках замість порожнього рядка поверталося значення **`false`** |

### Приклади

**Пример #1 Пример использования**grapheme\_substr()\*\*\*\*

```php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print urlencode(grapheme_substr( "ao" . $char_a_ring_nfd . "bc" . $char_o_diaeresis_nfd . "O", 2, -1 ));
?>
```

Результат виконання наведеного прикладу:

```
a%CC%8Abco%CC%88
```

### Дивіться також

-   [grapheme\_extract()](function.grapheme-extract.md) \- Функція для вилучення послідовності кластерів за замовчуванням графем з текстового буфера, яка повинна бути закодована в UTF-8
-   [»  Сегментація тексту в Unicode: межі кластера графеми](http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries)
