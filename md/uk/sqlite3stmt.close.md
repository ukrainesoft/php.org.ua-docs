---
navigation:
  - sqlite3stmt.clear.md: '« SQLite3Stmt::clear'
  - sqlite3stmt.construct.md: 'SQLite3Stmt::\_\_construct »'
  - index.md: PHP Manual
  - class.sqlite3stmt.md: SQLite3Stmt
title: 'SQLite3Stmt::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3Stmt::close

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::close — Закриває підготовлений запит

### Опис

```methodsynopsis
public SQLite3Stmt::close(): bool
```

Закриває запит.

> **Зауваження**: Зверніть увагу, що всі об'єкти [SQLite3Result](class.sqlite3result.md), отримані під час виконання цього підготовленого запиту будуть визнані недійсними під час закриття цього запиту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**
