---
navigation:
  - sqlite3.busytimeout.md: '« SQLite3::busyTimeout'
  - sqlite3.close.md: 'SQLite3::close »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::changes'
---
# SQLite3::changes

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::changes — Отримати кількість рядків, які були змінені/віддалені/вставлені останнім запитом

### Опис

```methodsynopsis
public SQLite3::changes(): int
```

Повертає кількість рядків, які були змінені/віддалені/вставлені останнім SQL-запитом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість рядків (int), які були змінені/віддалені/вставлені останнім SQL-запитом.

### Приклади

**Приклад #1 Приклад використання **SQLite3::changes()****

```php
<?php
$db = new SQLite3('mysqlitedb.db');

$query = $db->exec('UPDATE counter SET views=0 WHERE page="test"');
if ($query) {
    echo 'Количество изменённых строк: ', $db->changes();
}
?>
```
