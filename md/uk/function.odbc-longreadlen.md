---
navigation:
  - function.odbc-gettypeinfo.md: « odbc\_gettypeinfo
  - function.odbc-next-result.md: odbc\_next\_result »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_longreadlen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_longreadlen

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_longreadlen - Обробляє стовпці LONG

### Опис

```methodsynopsis
odbc_longreadlen(resource $statement, int $length): bool
```

Керує обробкою стовпців `LONG` `LONGVARCHAR`и`LONGVARBINARY`. Довжина за замовчуванням може бути встановлена ​​за допомогою директиви php.ini [uodbc.defaultlrl](odbc.configuration.md#ini.uodbc.defaultlrl)

### Список параметрів

`statement`

Ідентифікатор результату.

`length`

Кількість байтів, які повертаються PHP, контролюється довжиною параметра. Якщо встановлено значення дані стовпця LONG передаються клієнту (тобто друкуються) при отриманні за допомогою [odbc\_result()](function.odbc-result.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> На обработку столбцов`LONGVARBINARY` також впливає [odbc\_binmode()](function.odbc-binmode.md)
