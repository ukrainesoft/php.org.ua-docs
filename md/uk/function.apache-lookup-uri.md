Здійснити частковий запит на вказаний URI та повернути усі отримані відомості

-   [« apache\_getenv](function.apache-getenv.html)
    
-   [apache\_note »](function.apache-note.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Apache](ref.apache.html)
    
-   Здійснити частковий запит на вказаний URI та повернути усі отримані відомості
    

# apachelookupuri

(PHP 4, PHP 5, PHP 7, PHP 8)

apachelookupuri — Здійснити частковий запит на вказаний URI та повернути усі отримані відомості

### Опис

```methodsynopsis
apache_lookup_uri(string $filename): object|false
```

Ця функція здійснює частковий запит на вказаний URI. Цього достатньо для отримання всієї важливої ​​інформації про передану функцію ресурсу.

Ця функція підтримується лише якщо PHP встановлений як модуль Apache у веб-серверах.

### Список параметрів

`filename`

Ім'я файлу (URI), що запитується.

### Значення, що повертаються

Об'єкт, що містить інформацію про переданий URI. Властивістю даного об'єкта є:

-   status
-   therequest
-   statusline
-   метод
-   contenttype
-   handler
-   uri
-   filename
-   pathinfo
-   args
-   boundary
-   алеcache
-   алеlocalcopy
-   allowed
-   sendbodyct
-   bytessent
-   byterange
-   clength
-   unparseduri
-   mtime
-   requesttime

Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apachelookupuri()****

```php
<?php
$info = apache_lookup_uri('index.php?var=value');
print_r($info);

if (file_exists($info->filename)) {
    echo 'file exists!';
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

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