---
navigation:
  - sqlite3stmt.readonly.md: '« SQLite3Stmt::readOnly'
  - class.sqlite3result.md: SQLite3Result »
  - index.md: PHP Manual
  - class.sqlite3stmt.md: SQLite3Stmt
title: 'SQLite3Stmt::reset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3Stmt::reset

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::reset — Скидає підготовлений запит

### Опис

```methodsynopsis
public SQLite3Stmt::reset(): bool
```

Скидає підготовлений запит до стану до його виконання. Після скидання всі прив'язки залишаються незмінними.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у випадку, якщо підготовлений запит був успішно скинутий або \*\*`false`\*\*в случае возникновения ошибки.
