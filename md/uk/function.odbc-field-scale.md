---
navigation:
  - function.odbc-field-precision.md: « odbcfieldprecision
  - function.odbc-field-type.md: odbcfieldtype »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcfieldscale
---
# odbcfieldscale

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldscale — Повертає масштаб поля

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

Повертає масштаб поля у вигляді цілого чи числа **`false`** у разі виникнення помилки.
