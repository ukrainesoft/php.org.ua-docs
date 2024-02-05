---
navigation:
  - sqlite3.changes.md: '« SQLite3::changes'
  - sqlite3.construct.md: 'SQLite3::\_\_construct »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::close

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::close — Закрити з'єднання з базою даних

### Опис

```methodsynopsis
public SQLite3::close(): bool
```

Закриває з'єднання із БД.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SQLite3::close()\*\*\*\*

```php
<?php
$db = new SQLite3('mysqlitedb.db');
$db->close();
?>
```
