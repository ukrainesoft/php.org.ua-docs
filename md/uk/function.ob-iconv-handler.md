Перетворює символи з поточного кодування на кодування вихідного буфера

-   [« iconv](function.iconv.html)
    
-   [intl »](book.intl.html)
    
-   [PHP Manual](index.html)
    
-   [Функции iconv](ref.iconv.html)
    
-   Перетворює символи з поточного кодування на кодування вихідного буфера
    

# проiconvhandler

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

проiconvhandler — Перетворення символів із поточного кодування на кодування вихідного буфера

### Опис

```methodsynopsis
ob_iconv_handler(string $contents, int $status): string
```

Перетворює рядок, закодований у `internal_encoding`, у рядок, закодований у `output_encoding`

`internal_encoding` і `output_encoding` повинні бути визначені у php.ini або функцією [iconvsetencoding()](function.iconv-set-encoding.html)

### Список параметрів

Інформацію про аргументи цього обробника можна переглянути в описі функції [проstart()](function.ob-start.html)

### Значення, що повертаються

Інформацію про значення цього обробника, що повертаються, можна переглянути в описі до функції [проstart()](function.ob-start.html)

### Приклади

**Приклад #1 Приклад використання **проiconvhandler()****

```php
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
ob_start("ob_iconv_handler"); // запуск буферизации вывода
?>
```

### Дивіться також

-   [iconvgetencoding()](function.iconv-get-encoding.html) - Отримує поточне значення налаштувань перетворення кодувань
-   [iconvsetencoding()](function.iconv-set-encoding.html) - Встановлює поточні налаштування для перетворення символів кодування
-   [Функції контролю виведення](ref.outcontrol.html)