Отримує поточне значення параметрів перетворення кодувань

-   [« Функции iconv](ref.iconv.html)
    
-   [iconvmimedecodeheaders »](function.iconv-mime-decode-headers.html)
    
-   [PHP Manual](index.html)
    
-   [Функции iconv](ref.iconv.html)
    
-   Отримує поточне значення параметрів перетворення кодувань
    

# iconvgetencoding

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

iconvgetencoding — Отримує поточне значення параметрів перетворення кодувань

### Опис

```methodsynopsis
iconv_get_encoding(string $type = "all"): array|string|false
```

Повертає внутрішні параметри конфігурації модуля iconv.

### Список параметрів

`type`

Можливі значення необов'язкового параметра `type`

-   all
-   inputencoding
-   outputencoding
-   internalencoding

### Значення, що повертаються

Повертає поточне значення зазначеної змінної та **`false`** у разі виникнення помилки.

Якщо `type` не вказано або дорівнює "all", **iconvgetencoding()** поверне масив зі значеннями всіх змінних.

### Приклади

**Приклад #1 Приклад використання **iconvgetencoding()****

```php
<pre>
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("input_encoding", "WINDOWS-1251");
iconv_set_encoding("output_encoding", "KOI8-U");
var_dump(iconv_get_encoding('all'));
?>
</pre>
```

Результат виконання цього прикладу:

```
Array
(
    [input_encoding] => WINDOWS-1251
    [output_encoding] => KOI8-U
    [internal_encoding] => UTF-8
)
```

### Дивіться також

-   [iconvsetencoding()](function.iconv-set-encoding.html) - Встановлює поточні налаштування для перетворення символів кодування
-   [проiconvhandler()](function.ob-iconv-handler.html) - Перетворює символи з поточного кодування на кодування вихідного буфера