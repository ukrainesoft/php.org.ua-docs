---
navigation:
  - function.chr.md: « chr
  - function.convert-cyr-string.md: convertcyrstring »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: chunksplit
---
# chunksplit

(PHP 4, PHP 5, PHP 7, PHP 8)

chunksplit — Розбиває рядок на фрагменти

### Опис

```methodsynopsis
chunk_split(string $string, int $length = 76, string $separator = "\r\n"): string
```

Функція використовується для розбиття рядка на фрагменти, наприклад, для наведення результату функції [base64encode()](function.base64-encode.md) у відповідність до вимог RFC 2045. Вона вставляє рядок `separator` після кожних `length` символів.

### Список параметрів

`string`

Рядок, що розбивається.

`length`

Довжина фрагмента.

`separator`

Послідовність символів, що використовується як кінець рядка.

### Значення, що повертаються

Повертає перетворений рядок.

### Приклади

**Приклад #1 Приклад використання **chunksplit()****

```php
<?php
// форматирование данных в соответствии с RFC 2045
$new_string = chunk_split(base64_encode($data));
?>
```

### Дивіться також

-   [strsplit()](function.str-split.md) - Перетворює рядок на масив
-   [explode()](function.explode.md) - Розбиває рядок за допомогою роздільника
-   [wordwrap()](function.wordwrap.md) - Переносить рядок за вказаною кількістю символів
-   [» RFC 2045](http://www.faqs.org/rfcs/rfc2045)
