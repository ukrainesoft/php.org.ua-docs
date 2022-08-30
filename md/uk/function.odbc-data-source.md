Повертає інформацію про доступні DSN

-   [« odbccursor](function.odbc-cursor.html)
    
-   [odbcdo »](function.odbc-do.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає інформацію про доступні DSN
    

# odbcdatasource

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

odbcdatasource — Повертає інформацію про доступні DSN

### Опис

```methodsynopsis
odbc_data_source(resource $odbc, int $fetch_type): array|false
```

Ця функція поверне список доступних DSN (після кількох дзвінків).

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbcconnect()](function.odbc-connect.html)

`fetch_type`

`fetch_type` може бути одним з двох типів констант: **`SQL_FETCH_FIRST`** **`SQL_FETCH_NEXT`**. Використовуйте **`SQL_FETCH_FIRST`** при першому дзвінку цієї функції, після цього використовуйте **`SQL_FETCH_NEXT`**

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки, масив (array) у разі успішного виконання та **`null`** після вибору останнього доступного DSN.

### Приклади

**Приклад #1 Перелік доступних DSN**

```php
<?php
$conn = odbc_connect('dsn', 'user', 'pass');
$dsn_info = odbc_data_source($conn, SQL_FETCH_FIRST);
while ($dsn_info) {
    print_r($dsn_info);
    $dsn_info = odbc_data_source($conn, SQL_FETCH_NEXT);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

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