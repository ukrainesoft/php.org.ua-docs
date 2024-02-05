---
navigation:
  - function.odbc-fetch-row.md: « odbc\_fetch\_row
  - function.odbc-field-name.md: odbc\_field\_name »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_field\_len
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_field\_len

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_field\_len — Повертає довжину (точність) поля

### Опис

```methodsynopsis
odbc_field_len(resource $statement, int $field): int|false
```

Повертає довжину поля, на яке посилається число у заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Номер поля. Нумерація полів починається з першого.

### Значення, що повертаються

Повертає довжину поля або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [odbc\_field\_scale()](function.odbc-field-scale.md) \- Повертає масштаб поля для набуття масштабу числа з плаваючою точкою
