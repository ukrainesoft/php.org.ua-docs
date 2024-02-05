---
navigation:
  - function.odbc-next-result.md: « odbc\_next\_result
  - function.odbc-num-rows.md: odbc\_num\_rows »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_num\_fields

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_num\_fields — Повертає кількість стовпців у результаті

### Опис

```methodsynopsis
odbc_num_fields(resource $statement): int
```

Повертає кількість полів (стовпців) у результаті ODBC.

### Список параметрів

`statement`

Ідентифікатор результату, що повертається [odbc\_exec()](function.odbc-exec.md)

### Значення, що повертаються

Повертає кількість полів або -1 у разі помилки.
