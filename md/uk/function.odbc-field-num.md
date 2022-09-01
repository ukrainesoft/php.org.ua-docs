---
navigation:
  - function.odbc-field-name.html: « odbcfieldname
  - function.odbc-field-precision.html: odbcfieldprecision »
  - index.html: PHP Manual
  - ref.uodbc.html: Функции ODBC
title: odbcfieldnum
---
# odbcfieldnum

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldnum — Повертає номер стовпця

### Опис

```methodsynopsis
odbc_field_num(resource $statement, string $field): int|false
```

Отримує номер слота стовпця, який відповідає полю в заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Ім'я поля.

### Значення, що повертаються

Повертає номер поля у вигляді цілого чи числа **`false`** у разі виникнення помилки. Нумерація полів починається з першого.
