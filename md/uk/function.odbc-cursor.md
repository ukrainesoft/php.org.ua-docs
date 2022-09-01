---
navigation:
  - function.odbc-connect.html: « odbcconnect
  - function.odbc-data-source.html: odbcdatasource »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbccursor
---
# odbccursor

(PHP 4, PHP 5, PHP 7, PHP 8)

odbccursor — Повертає ім'я курсору

### Опис

```methodsynopsis
odbc_cursor(resource $statement): string|false
```

Повертає ім'я курсору для даного resultid.

### Список параметрів

`statement`

Ідентифікатор результату.

### Значення, що повертаються

Повертає ім'я курсора у вигляді рядка або **`false`** у разі виникнення помилки.
