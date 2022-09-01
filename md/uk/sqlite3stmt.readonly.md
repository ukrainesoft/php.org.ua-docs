---
navigation:
  - sqlite3stmt.paramcount.md: '« SQLite3Stmt::paramCount'
  - sqlite3stmt.reset.md: 'SQLite3Stmt::reset »'
  - index.md: PHP Manual
  - class.sqlite3stmt.md: SQLite3Stmt
title: 'SQLite3Stmt::readOnly'
---
# SQLite3Stmt::readOnly

(PHP 5> = 5.3.6, PHP 7, PHP 8)

SQLite3Stmt::readOnly — Перевіряє, чи підготовлений запит лише для читання

### Опис

```methodsynopsis
public SQLite3Stmt::readOnly(): bool
```

Повертає, чи є підготовлений запит безперечно лише для читання. Запит вважається тільки для читання, якщо він не вносить *безпосередніх* змін до вмісту файлу бази даних. Зверніть увагу, що користувацькі SQL-функції можуть *опосередковано* змінювати базу даних як побічний ефект.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо запит лише для читання, **`false`** в іншому випадку.
