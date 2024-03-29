---
navigation:
  - function.odbc-primarykeys.md: « odbc\_primarykeys
  - function.odbc-procedures.md: odbc\_procedures »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_procedurecolumns
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_procedurecolumns

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_procedurecolumns — Отримує інформацію про параметри процедур

### Опис

```methodsynopsis
odbc_procedurecolumns(    resource $odbc,    ?string $catalog = null,    ?string $schema = null,    ?string $procedure = null,    ?string $column = null): resource|false
```

Отримує інформацію про параметри процедури.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2). Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`procedure`

Процедура. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`column`

Стовпець. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

### Значення, що повертаються

Повертає список вхідних та вихідних параметрів, а також стовпці, що становлять результуючий набір для зазначених процедур. Повертає ідентифікатор результату ODBC або \*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   `PROCEDURE_CAT`
-   `PROCEDURE_SCHEM`
-   `PROCEDURE_NAME`
-   `COLUMN_NAME`
-   `COLUMN_TYPE`
-   `DATA_TYPE`
-   `TYPE_NAME`
-   `COLUMN_SIZE`
-   `BUFFER_LENGTH`
-   `DECIMAL_DIGITS`
-   `NUM_PREC_RADIX`
-   `NULLABLE`
-   `REMARKS`
-   `COLUMN_DEF`
-   `SQL_DATA_TYPE`
-   `SQL_DATETIME_SUB`
-   `CHAR_OCTET_LENGTH`
-   `ORDINAL_POSITION`
-   `IS_NULLABLE`

Драйвери можуть повідомляти додаткові стовпці.

Результирующий набор упорядочивается по`PROCEDURE_CAT` `PROCEDURE_SCHEM` `PROCEDURE_NAME`и`COLUMN_TYPE`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | До цієї версії функцію можна було викликати лише з одним або п'ятьма аргументами. |

### Приклади

**Приклад #1 Перелік стовпців процедури, що зберігається**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$columns = odbc_procedurecolumns($conn, 'TutorialDB', 'dbo', 'GetEmployeeSalesYTD;1', '%');
while (($row = odbc_fetch_array($columns))) {
    print_r($row);
    break; // последующие строки опущены для краткости
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [PROCEDURE_CAT] => TutorialDB
    [PROCEDURE_SCHEM] => dbo
    [PROCEDURE_NAME] => GetEmployeeSalesYTD;1
    [COLUMN_NAME] => @SalesPerson
    [COLUMN_TYPE] => 1
    [DATA_TYPE] => -9
    [TYPE_NAME] => nvarchar
    [COLUMN_SIZE] => 50
    [BUFFER_LENGTH] => 100
    [DECIMAL_DIGITS] =>
    [NUM_PREC_RADIX] =>
    [NULLABLE] => 1
    [REMARKS] =>
    [COLUMN_DEF] =>
    [SQL_DATA_TYPE] => -9
    [SQL_DATETIME_SUB] =>
    [CHAR_OCTET_LENGTH] => 100
    [ORDINAL_POSITION] => 1
    [IS_NULLABLE] => YES
)
```

### Дивіться також

-   [odbc\_columns()](function.odbc-columns.md) \- перераховує імена стовпців у зазначених таблицях
