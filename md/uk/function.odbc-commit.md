---
navigation:
  - function.odbc-columns.md: « odbc\_columns
  - function.odbc-connect.md: odbc\_connect »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_commit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_commit

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_commit - Фіксує транзакцію ODBC

### Опис

```methodsynopsis
odbc_commit(resource $odbc): bool
```

Фіксує всі незавершені транзакції з'єднання.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
