---
navigation:
  - sqlite3result.columnname.md: '« SQLite3Result::columnName'
  - sqlite3result.construct.md: 'SQLite3Result::\_\_construct »'
  - index.md: PHP Manual
  - class.sqlite3result.md: SQLite3Result
title: 'SQLite3Result::columnType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3Result::columnType

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3Result::columnType — Повертає тип n-ного стовпця

### Опис

```methodsynopsis
public SQLite3Result::columnType(int $column): int|false
```

Повертає тип стовпця, вказаного в `column`

### Список параметрів

`column`

Номер стовпця, починаючи з нуля.

### Значення, що повертаються

Повертає тип стовпця, вказаного в `column`. Повертає значення **`SQLITE3_INTEGER`** **`SQLITE3_FLOAT`** **`SQLITE3_TEXT`** **`SQLITE3_BLOB`** **`SQLITE3_NULL`**) или\*\*`false`\*\*якщо стовпець не існує.
