---
navigation:
  - sqlite3.escapestring.md: '« SQLite3::escapeString'
  - sqlite3.lasterrorcode.md: 'SQLite3::lastErrorCode »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::exec'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::exec

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::exec — Виконує запит без результату до поточної бази даних

### Опис

```methodsynopsis
public SQLite3::exec(string $query): bool
```

Виконує запит без результату до поточної бази даних.

> **Зауваження**: SQLite3, можливо, потрібно створити [" тимчасові файли](https://sqlite.org/tempfiles.md) під час виконання запитів, тому відповідні директорії повинні бути доступні для запису.

### Список параметрів

`query`

Запит SQL, що виконується (зазвичай запит INSERT, UPDATE або DELETE).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання запиту або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SQLite3::exec()\*\*\*\*

```php
<?php
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE bar (bar TEXT)');
?>
```
