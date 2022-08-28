Набір символів MIME

-   [« mb\_parse\_str](function.mb-parse-str.html)
    
-   [mb\_regex\_encoding »](function.mb-regex-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Набір символів MIME
    

# мбpreferredmimename

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбpreferredmimename — Отримання набору символів MIME

### Опис

```methodsynopsis
mb_preferred_mime_name(string $encoding): string|false
```

Отримує рядок (string) набору символів MIME для кодування.

### Список параметрів

`encoding`

Кодування, для якого вибирається набір символів.

### Значення, що повертаються

MIME-набір символів `charset` у вигляді рядка (string) для кодування `encoding` або **`false`**, якщо для заданого кодування `encoding` немає кращого набору символів.

### Приклади

**Приклад #1 Приклад використання **мбpreferredmimename()****

```php
<?php
$outputenc = "sjis-win";
mb_http_output($outputenc);
ob_start("mb_output_handler");
header("Content-Type: text/html; charset=" . mb_preferred_mime_name($outputenc));
?>
```