---
navigation:
  - ref.iconv.md: « Функції iconv
  - function.iconv-mime-decode-headers.md: iconv\_mime\_decode\_headers »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: iconv\_get\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iconv\_get\_encoding

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

iconv\_get\_encoding — Отримує поточне значення параметрів перетворення кодувань

### Опис

```methodsynopsis
iconv_get_encoding(string $type = "all"): array|string|false
```

Повертає внутрішні параметри конфігурації модуля iconv.

### Список параметрів

`type`

Можливі значення необов'язкового параметра `type` :

-   all
-   input\_encoding
-   output\_encoding
-   internal\_encoding

### Значення, що повертаються

Повертає поточне значення зазначеної змінної та \*\*`false`\*\*в случае возникновения ошибки.

Якщо `type` не вказано або дорівнює "all", **iconv\_get\_encoding()** поверне масив зі значеннями всіх змінних.

### Приклади

**Пример #1 Пример использования**iconv\_get\_encoding()\*\*\*\*

```php
<pre>
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("input_encoding", "WINDOWS-1251");
iconv_set_encoding("output_encoding", "KOI8-U");
var_dump(iconv_get_encoding('all'));
?>
</pre>
```

Результат виконання наведеного прикладу:

```
Array
(
    [input_encoding] => WINDOWS-1251
    [output_encoding] => KOI8-U
    [internal_encoding] => UTF-8
)
```

### Дивіться також

-   [iconv\_set\_encoding()](function.iconv-set-encoding.md) \- Встановлює поточні налаштування для перетворення символів кодування
-   [ob\_iconv\_handler()](function.ob-iconv-handler.md) \- Перетворює символи з поточного кодування на кодування вихідного буфера
