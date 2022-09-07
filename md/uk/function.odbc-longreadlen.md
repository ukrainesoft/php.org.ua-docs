---
navigation:
  - function.odbc-gettypeinfo.md: « odbcgettypeinfo
  - function.odbc-next-result.md: odbcnextresult »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbclongreadlen
---
# odbclongreadlen

(PHP 4, PHP 5, PHP 7, PHP 8)

odbclongreadlen - Обробляє стовпці LONG

### Опис

```methodsynopsis
odbc_longreadlen(resource $statement, int $length): bool
```

Керує обробкою стовпців `LONG` `LONGVARCHAR` і `LONGVARBINARY`. Довжина за замовчуванням може бути встановлена ​​за допомогою директиви php.ini [uodbc.defaultlrl](odbc.configuration.md#ini.uodbc.defaultlrl)

### Список параметрів

`statement`

Ідентифікатор результату.

`length`

Кількість байтів, які повертаються PHP, контролюється довжиною параметра. Якщо встановлено значення `0`дані стовпця LONG передаються клієнту (тобто друкуються) при отриманні за допомогою [odbcresult()](function.odbc-result.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> На обробку стовпців `LONGVARBINARY` також впливає [odbcbinmode()](function.odbc-binmode.md)
