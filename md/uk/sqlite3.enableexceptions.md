---
navigation:
  - sqlite3.createfunction.md: '« SQLite3::createFunction'
  - sqlite3.escapestring.md: 'SQLite3::escapeString »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::enableExceptions'
---
# SQLite3::enableExceptions

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::enableExceptions — Увімкнути викид винятків

### Опис

```methodsynopsis
public SQLite3::enableExceptions(bool $enable = false): bool
```

Визначає, чи буде екземпляр [SQLite3](class.sqlite3.md) викидати винятки чи попередження про помилку.

### Список параметрів

`enable`

Коли передано значення **`true`**, екземпляр [SQLite3](class.sqlite3.md) та екземпляри [SQLite3Stmt](class.sqlite3stmt.md) і [SQLite3Result](class.sqlite3result.md), похідні від нього, викидатимуть винятки у разі виникнення помилки.

Коли передано значення **`false`**, екземпляр [SQLite3](class.sqlite3.md) та екземпляри [SQLite3Stmt](class.sqlite3stmt.md) і [SQLite3Result](class.sqlite3result.md), похідні від нього, генеруватимуть попередження у разі виникнення помилки.

У будь-якому випадку код помилки та повідомлення, якщо вони є, будуть доступні через [SQLite3::lastErrorCode()](sqlite3.lasterrorcode.md) і [SQLite3::lastErrorMsg()](sqlite3.lasterrormsg.md) відповідно.

### Значення, що повертаються

Повертає старе значення; \*\*`true`\*\*якщо винятки включені, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SQLite3::enableExceptions()****

```php
<?php
$sqlite = new SQLite3(':memory:');
try {
    $sqlite->exec('create table foo');
    $sqlite->enableExceptions(true);
    $sqlite->exec('create table bar');
} catch (Exception $e) {
    echo 'Поймано исключение: ' . $e->getMessage();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Warning: SQLite3::exec(): near "foo": syntax error in example.php on line 4
Поймано исключение: near "bar": syntax error
```
