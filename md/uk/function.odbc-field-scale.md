---
navigation:
  - function.odbc-field-precision.md: « odbc\_field\_precision
  - function.odbc-field-type.md: odbc\_field\_type »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_field\_scale
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_field\_scale

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_field\_scale — Повертає масштаб поля

### Опис

```methodsynopsis
odbc_field_scale(resource $statement, int $field): int|false
```

Повертає масштаб поля, на яке посилається число у заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Номер поля. Нумерація полів починається з першого.

### Значення, що повертаються

Повертає масштаб поля у вигляді цілого чи числа \*\*`false`\*\*в случае возникновения ошибки.
