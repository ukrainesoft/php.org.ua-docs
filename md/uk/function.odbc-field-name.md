---
navigation:
  - function.odbc-field-len.md: « odbc\_field\_len
  - function.odbc-field-num.md: odbc\_field\_num »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_field\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_field\_name

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_field\_name — Повертає ім'я стовпця

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

Повертає ім'я поля у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.
