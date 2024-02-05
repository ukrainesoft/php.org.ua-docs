---
navigation:
  - sqlite3.openblob.md: '« SQLite3::openBlob'
  - sqlite3.query.md: 'SQLite3::query »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::prepare'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::prepare

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::prepare — Підготовка SQL-запиту для виконання

### Опис

```methodsynopsis
public SQLite3::prepare(string $query): SQLite3Stmt|false
```

Підготовляє SQL-запит для виконання та повертає об'єкт [SQLite3Stmt](class.sqlite3stmt.md)

### Список параметрів

`query`

SQL запит на підготовку.

### Значення, що повертаються

Повертає об'єкт [SQLite3Stmt](class.sqlite3stmt.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SQLite3::prepare()\*\*\*\*

```php
<?php
unlink('mysqlitedb.db');
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE foo (id INTEGER, bar STRING)');
$db->exec("INSERT INTO foo (id, bar) VALUES (1, 'Тестовое значение')");

$stmt = $db->prepare('SELECT bar FROM foo WHERE id=:id');
$stmt->bindValue(':id', 1, SQLITE3_INTEGER);

$result = $stmt->execute();
var_dump($result->fetchArray());
?>
```

### Дивіться також

-   [SQLite3Stmt::paramCount()](sqlite3stmt.paramcount.md) \- Повертає кількість параметрів у підготовленому запиті
-   [SQLite3Stmt::bindValue()](sqlite3stmt.bindvalue.md) \- Зв'язує значення параметра зі змінною підготовленого запиту
-   [SQLite3Stmt::bindParam()](sqlite3stmt.bindparam.md) \- Зв'язує параметр із змінною підготовленого запиту
