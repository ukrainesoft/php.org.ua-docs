---
navigation:
  - function.odbc-cursor.md: « odbc\_cursor
  - function.odbc-do.md: odbc\_do »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_data\_source
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_data\_source

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

odbc\_data\_source — Повертає інформацію про доступні DSN

### Опис

```methodsynopsis
odbc_data_source(resource $odbc, int $fetch_type): array|false
```

Ця функція поверне список доступних DSN (після кількох дзвінків).

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`fetch_type`

`fetch_type` може бути одним з двох типів констант: **`SQL_FETCH_FIRST`** **`SQL_FETCH_NEXT`**Используйте**`SQL_FETCH_FIRST`** при першому дзвінку цієї функції, після цього використовуйте **`SQL_FETCH_NEXT`**

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки, масив (array) у разі успішного виконання та **`null`** після вибору останнього доступного DSN.

### Приклади

**Приклад #1 Перелік доступних DSN**

```php
<?php
$conn = odbc_connect('dsn', 'user', 'pass');
$dsn_info = odbc_data_source($conn, SQL_FETCH_FIRST);
while ($dsn_info) {
    print_r($dsn_info);
    $dsn_info = odbc_data_source($conn, SQL_FETCH_NEXT);
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [server] => dsn
    [description] => ODBC Driver 17 for SQL Server
)
Array
(
    [server] => other_dsn
    [description] => Microsoft Access Driver (*.mdb, *.accdb)
)
```
