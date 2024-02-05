---
navigation:
  - function.mb-parse-str.md: « mb\_parse\_str
  - function.mb-regex-encoding.md: mb\_regex\_encoding »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_preferred\_mime\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_preferred\_mime\_name

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_preferred\_mime\_name — Отримує рядок кодування MIME

### Опис

```methodsynopsis
mb_preferred_mime_name(string $encoding): string|false
```

Отримує рядок (string) MIME кодування для заданого кодування.

### Список параметрів

`encoding`

Кодування.

### Значення, що повертаються

Повертає MIME-кодування `charset` у вигляді рядка (string) для кодування символів `encoding`, или\*\*`false`\*\*, якщо кодування `encoding` Не можна зіставити MIME-кодування.

### Приклади

**Пример #1 Пример использования функции**mb\_preferred\_mime\_name()\*\*\*\*

```php
<?php

$outputenc = "sjis-win";
mb_http_output($outputenc);
ob_start("mb_output_handler");
header("Content-Type: text/html; charset=" . mb_preferred_mime_name($outputenc));
?>
```
