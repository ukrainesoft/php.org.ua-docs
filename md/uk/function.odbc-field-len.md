---
navigation:
  - function.odbc-fetch-row.md: « odbcfetchrow
  - function.odbc-field-name.md: odbcfieldname »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcfieldlen
---
# odbcfieldlen

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldlen — Повертає довжину (точність) поля

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

Повертає довжину поля або **`false`** у разі виникнення помилки.

### Дивіться також

-   [odbcfieldscale()](function.odbc-field-scale.md) - Повертає масштаб поля для набуття масштабу числа з плаваючою точкою
