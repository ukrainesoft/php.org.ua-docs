---
navigation:
  - function.odbc-num-fields.md: « odbc\_num\_fields
  - function.odbc-pconnect.md: odbc\_pconnect »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_num\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_num\_rows

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_num\_rows — Повертає кількість рядків у результаті

### Опис

```methodsynopsis
odbc_num_rows(resource $statement): int
```

Повертає кількість рядків у результаті. Для операторів INSERT, UPDATE та DELETE **odbc\_num\_rows()** повертає кількість порушених рядків. Для пропозиції SELECT це `може` бути кількість доступних рядків.

### Список параметрів

`statement`

Ідентифікатор результату, що повертається [odbc\_exec()](function.odbc-exec.md)

### Значення, що повертаються

Повертає кількість рядків у результаті ODBC. Функція поверне -1 у разі виникнення помилки.

### Примітки

> **Зауваження** :
> 
> Использование**odbc\_num\_rows()** для визначення кількості рядків, доступних після виконання SELECT поверне -1 для багатьох драйверів.
