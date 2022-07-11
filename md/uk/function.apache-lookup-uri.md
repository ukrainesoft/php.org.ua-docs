- [« apache_getenv](function.apache-getenv.md)
- [apache_note »](function.apache-note.md)

- [PHP Manual](index.md)
- [Функції Apache](ref.apache.md)
- Здійснити частковий запит на вказаний URI та повернути все
отримані відомості

#apache_lookup_uri

(PHP 4, PHP 5, PHP 7, PHP 8)

apache_lookup_uri — Здійснити частковий запит на вказаний URI та
повернути усі отримані відомості

### Опис

**apache_lookup_uri**(string `$filename`): object\|false

Ця функція здійснює частковий запит на вказаний URI. Цього
достатньо для отримання всієї важливої інформації про передану функцію
ресурс.

Ця функція підтримується лише якщо PHP встановлено як модуль
Apache у веб-серверах.

### Список параметрів

`filename`
Ім'я файлу (URI), що запитується.

### Значення, що повертаються

Об'єкт, що містить інформацію про передане URI. Властивістю даного
об'єкти є:

- status
- the_request
- status_line
- method
- content_type
- handler
- uri
- filename
- path_info
- args
- boundary
- no_cache
- no_local_copy
- allowed
- send_bodyct
- bytes_sent
- byterange
- clength
- unparsed_uri
- mtime
- request_time

Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apache_lookup_uri()****

` <?php$info = apache_lookup_uri('index.php?var=value');print_r($info);if (file_exists($info->filename)) {    echo 'file exists!';}?> `

Результатом виконання цього прикладу буде щось подібне:

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
