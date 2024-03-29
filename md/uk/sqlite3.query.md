---
navigation:
  - sqlite3.prepare.md: '« SQLite3::prepare'
  - sqlite3.querysingle.md: 'SQLite3::querySingle »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::query'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::query

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::query — Виконує SQL-запит

### Опис

```methodsynopsis
public SQLite3::query(string $query): SQLite3Result|false
```

Виконує SQL-запит та повертає об'єкт [SQLite3Result](class.sqlite3result.md). Якщо запит не повертає результат (наприклад, запит типу DLM), то повернутий об'єкт [SQLite3Result](class.sqlite3result.md) марний. Для таких запитів використовуйте метод [SQLite3::exec()](sqlite3.exec.md)

### Список параметрів

`query`

SQL-запит для виконання.

### Значення, що повертаються

Повертає об'єкт [SQLite3Result](class.sqlite3result.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SQLite3::query()\*\*\*\*

```php
<?php
$db = new SQLite3('mysqlitedb.db');

$results = $db->query('SELECT bar FROM foo');
while ($row = $results->fetchArray()) {
    var_dump($row);
}
?>
```
