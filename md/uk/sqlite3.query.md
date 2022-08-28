Виконує SQL-запит

-   [« SQLite3::prepare](sqlite3.prepare.html)
    
-   [SQLite3::querySingle »](sqlite3.querysingle.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3](class.sqlite3.html)
    
-   Виконує SQL-запит
    

# SQLite3::query

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::query — Виконує SQL-запит

### Опис

```methodsynopsis
public SQLite3::query(string $query): SQLite3Result|false
```

Виконує SQL-запит та повертає об'єкт [SQLite3Result](class.sqlite3result.html). Якщо запит не повертає результат (наприклад, запит типу DLM), то повернутий об'єкт [SQLite3Result](class.sqlite3result.html) марний. Для таких запитів використовуйте метод [SQLite3::exec()](sqlite3.exec.html)

### Список параметрів

`query`

SQL-запит для виконання.

### Значення, що повертаються

Повертає об'єкт [SQLite3Result](class.sqlite3result.html) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SQLite3::query()****

```php
<?php
$db = new SQLite3('mysqlitedb.db');

$results = $db->query('SELECT bar FROM foo');
while ($row = $results->fetchArray()) {
    var_dump($row);
}
?>
```