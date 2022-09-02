---
navigation:
  - function.odbc-field-len.md: « odbcfieldlen
  - function.odbc-field-num.md: odbcfieldnum »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcfieldname
---
# odbcfieldname

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfieldname — Повертає ім'я стовпця

### Опис

```methodsynopsis
odbc_field_name(resource $statement, int $field): string|false
```

Повертає ім'я поля, що займає номер стовпця в заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Номер поля. Нумерація полів починається з першого.

### Значення, що повертаються

Повертає ім'я поля у вигляді рядка або **`false`** у разі виникнення помилки.
