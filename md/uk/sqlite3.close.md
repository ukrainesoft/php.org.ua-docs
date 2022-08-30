Закрити з'єднання з базою даних

-   [« SQLite3::changes](sqlite3.changes.html)
    
-   [SQLite3::construct »](sqlite3.construct.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3](class.sqlite3.html)
    
-   Закрити з'єднання з базою даних
    

# SQLite3::close

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::close — Закрити з'єднання з базою даних

### Опис

```methodsynopsis
public SQLite3::close(): bool
```

Закриває з'єднання із БД.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SQLite3::close()****

```php
<?php
$db = new SQLite3('mysqlitedb.db');
$db->close();
?>
```