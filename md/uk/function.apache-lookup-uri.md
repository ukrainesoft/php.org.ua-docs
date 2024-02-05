---
navigation:
  - function.apache-getenv.md: « apache\_getenv
  - function.apache-note.md: apache\_note »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_lookup\_uri
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_lookup\_uri

(PHP 4, PHP 5, PHP 7, PHP 8)

apache\_lookup\_uri — Здійснити частковий запит на вказаний URI та повернути усі отримані відомості

### Опис

```methodsynopsis
apache_lookup_uri(string $filename): object|false
```

Ця функція здійснює частковий запит на вказаний URI. Цього достатньо для отримання всієї важливої ​​інформації про функцію переданого ресурсу.

Ця функція підтримується лише якщо PHP встановлений як модуль Apache у веб-серверах.

### Список параметрів

`filename`

Ім'я файлу (URI), що запитується.

### Значення, що повертаються

Об'єкт, що містить інформацію про переданий URI. Властивістю даного об'єкта є:

-   status
-   the\_request
-   status\_line
-   method
-   content\_type
-   handler
-   uri
-   filename
-   path\_info
-   args
-   boundary
-   no\_cache
-   no\_local\_copy
-   allowed
-   send\_bodyct
-   bytes\_sent
-   byterange
-   clength
-   unparsed\_uri
-   mtime
-   request\_time

Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**apache\_lookup\_uri()\*\*\*\*

```php
<?php
$info = apache_lookup_uri('index.php?var=value');
print_r($info);

if (file_exists($info->filename)) {
    echo 'file exists!';
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
stdClass Object
(
    [status] => 200
    [the_request] => GET /dir/file.php HTTP/1.1
    [method] => GET
    [mtime] => 0
    [clength] => 0
    [chunked] => 0
    [content_type] => application/x-httpd-php
    [no_cache] => 0
    [no_local_copy] => 1
    [unparsed_uri] => /dir/index.php?var=value
    [uri] => /dir/index.php
    [filename] => /home/htdocs/dir/index.php
    [args] => var=value
    [allowed] => 0
    [sent_bodyct] => 0
    [bytes_sent] => 0
    [request_time] => 1074282764
)
file exists!
```
