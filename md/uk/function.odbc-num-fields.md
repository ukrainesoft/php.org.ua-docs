---
navigation:
  - function.odbc-next-result.md: « odbcnextresult
  - function.odbc-num-rows.md: odbcnumrows »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcnumfields
---
# odbcnumfields

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcnumfields — Повертає кількість стовпців у результаті

### Опис

```methodsynopsis
odbc_num_fields(resource $statement): int
```

Повертає кількість полів (стовпців) у результаті ODBC.

### Список параметрів

`statement`

Ідентифікатор результату, що повертається [odbcexec()](function.odbc-exec.md)

### Значення, що повертаються

Повертає кількість полів або -1 у разі помилки.
