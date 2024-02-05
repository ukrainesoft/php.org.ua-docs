---
navigation:
  - function.odbc-connection-string-should-quote.md: « odbc\_connection\_string\_should\_quote
  - function.odbc-data-source.md: odbc\_data\_source »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_cursor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_cursor

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_cursor — Повертає ім'я курсору

### Опис

```methodsynopsis
odbc_cursor(resource $statement): string|false
```

Повертає ім'я курсору для даного result\_id.

### Список параметрів

`statement`

Ідентифікатор результату.

### Значення, що повертаються

Повертає ім'я курсора у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.
