---
navigation:
  - function.odbc-columns.html: « odbccolumns
  - function.odbc-connect.html: odbcconnect »
  - index.html: PHP Manual
  - ref.uodbc.html: Функции ODBC
title: odbccommit
---
# odbccommit

(PHP 4, PHP 5, PHP 7, PHP 8)

odbccommit - Фіксує транзакцію ODBC

### Опис

```methodsynopsis
odbc_commit(resource $odbc): bool
```

Фіксує всі незавершені транзакції з'єднання.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
