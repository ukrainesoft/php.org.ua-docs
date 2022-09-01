---
navigation:
  - sqlite3.escapestring.html: '« SQLite3::escapeString'
  - sqlite3.lasterrorcode.html: 'SQLite3::lastErrorCode »'
  - index.html: PHP Manual
  - class.sqlite3.html: SQLite3
title: 'SQLite3::exec'
---
# SQLite3::exec

(PHP 5> = 5.3.0, PHP 7, PHP 8)

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

Повертає **`true`** у разі успішного виконання запиту або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SQLite3::exec()****

```php
<?php
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE bar (bar TEXT)');
?>
```
