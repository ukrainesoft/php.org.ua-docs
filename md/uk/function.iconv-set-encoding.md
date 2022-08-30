Встановлює поточні налаштування для перетворення символів кодування

-   [« iconvmimeencode](function.iconv-mime-encode.html)
    
-   [iconvstrlen »](function.iconv-strlen.html)
    
-   [PHP Manual](index.md)
    
-   [Функции iconv](ref.iconv.md)
    
-   Встановлює поточні налаштування для перетворення символів кодування
    

# iconvsetencoding

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

iconvsetencoding — Встановлює поточні налаштування для перетворення символів кодування

### Опис

```methodsynopsis
iconv_set_encoding(string $type, string $encoding): bool
```

Змінює значення вказаної параметром `type` внутрішньої змінної конфігурації на `encoding`

### Список параметрів

`type`

Значення `type` може бути одним із наведених нижче:

-   inputencoding
-   outputencoding
-   internalencoding

`encoding`

Набір символів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **iconvsetencoding()****

```php
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
?>
```

### Дивіться також

-   [iconvgetencoding()](function.iconv-get-encoding.html) - Отримує поточне значення налаштувань перетворення кодувань
-   [проiconvhandler()](function.ob-iconv-handler.html) - Перетворює символи з поточного кодування на кодування вихідного буфера