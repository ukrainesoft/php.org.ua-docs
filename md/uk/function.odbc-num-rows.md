---
navigation:
  - function.odbc-num-fields.md: « odbcnumfields
  - function.odbc-pconnect.md: odbcpconnect »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
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

Ідентифікатор результату, що повертається [odbcexec()](function.odbc-exec.md)

### Значення, що повертаються

Повертає кількість рядків у результаті ODBC. Функція поверне -1 у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Використання **odbcnumrows()** для визначення кількості рядків, доступних після виконання SELECT поверне -1 для багатьох драйверів.
