---
navigation:
  - sqlite3.lasterrormsg.md: '« SQLite3::lastErrorMsg'
  - sqlite3.loadextension.md: 'SQLite3::loadExtension »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::lastInsertRowID'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::lastInsertRowID

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::lastInsertRowID — Повертає ідентифікатор рядка останньої вставки (INSERT) до бази даних

### Опис

```methodsynopsis
public SQLite3::lastInsertRowID(): int
```

Повертає ідентифікатор рядка останньої вставки (INSERT) до бази даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор рядка останньої вставки (INSERT) до бази даних. Якщо при цьому з'єднанні з базою даних ніколи не відбувалося успішних операцій INSERT у таблиці rowid, то **SQLite3::lastInsertRowID()** повертає
