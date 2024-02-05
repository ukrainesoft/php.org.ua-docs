---
navigation:
  - function.odbc-field-scale.md: « odbc\_field\_scale
  - function.odbc-foreignkeys.md: odbc\_foreignkeys »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_field\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_field\_type

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_field\_type — Повертає тип даних поля

### Опис

```methodsynopsis
odbc_field_type(resource $statement, int $field): string|false
```

Отримує SQL тип поля, на яке посилається число в заданому ідентифікаторі результату.

### Список параметрів

`statement`

Ідентифікатор результату.

`field`

Номер поля. Нумерація полів починається з першого.

### Значення, що повертаються

Повертає тип поля у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.
