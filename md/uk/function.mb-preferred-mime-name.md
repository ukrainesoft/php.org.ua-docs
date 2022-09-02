---
navigation:
  - function.mb-parse-str.md: « mbparsestr
  - function.mb-regex-encoding.md: мбregexencoding »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбpreferredmimename
---
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
