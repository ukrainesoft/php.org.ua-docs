---
navigation:
  - function.odbc-num-fields.html: « odbcnumfields
  - function.odbc-pconnect.html: odbcpconnect »
  - index.html: PHP Manual
  - ref.uodbc.html: Функции ODBC
title: odbcnumrows
---
# odbcnumrows

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcnumrows — Повертає кількість рядків у результаті

### Опис

```methodsynopsis
odbc_num_rows(resource $statement): int
```

Повертає кількість рядків у результаті. Для операторів INSERT, UPDATE та DELETE **odbcnumrows()** повертає кількість порушених рядків. Для пропозиції SELECT це `может` бути кількість доступних рядків.

### Список параметрів

`statement`

Ідентифікатор результату, що повертається [odbcexec()](function.odbc-exec.html)

### Значення, що повертаються

Повертає кількість рядків у результаті ODBC. Функція поверне -1 у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Використання **odbcnumrows()** для визначення кількості рядків, доступних після виконання SELECT поверне -1 для багатьох драйверів.
