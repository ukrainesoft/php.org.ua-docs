---
navigation:
  - function.odbc-field-name.md: « odbc\_field\_name
  - function.odbc-field-precision.md: odbc\_field\_precision »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_field\_num
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_field\_num

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_field\_num — Повертає номер стовпця

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

Повертає номер поля у вигляді цілого чи числа \*\*`false`\*\*в случае возникновения ошибки. Нумерация полей начинается с 1.
