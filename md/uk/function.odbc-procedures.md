---
navigation:
  - function.odbc-procedurecolumns.md: « odbc\_procedurecolumns
  - function.odbc-result-all.md: odbc\_result\_all »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_procedures
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_procedures

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_procedures — Отримує список процедур, які зберігаються у певному джерелі даних

### Опис

```methodsynopsis
odbc_procedures(    resource $odbc,    ?string $catalog = null,    ?string $schema = null,    ?string $procedure = null): resource|false
```

Перелічує всі процедури у запрошеному діапазоні.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2). Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`procedure`

Ім'я процедури. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

### Значення, що повертаються

Возвращает идентификатор результата ODBC, содержащий информацию или\*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   `PROCEDURE_CAT`
-   `PROCEDURE_SCHEM`
-   `PROCEDURE_NAME`
-   `NUM_INPUT_PARAMS`
-   `NUM_OUTPUT_PARAMS`
-   `NUM_RESULT_SETS`
-   `REMARKS`
-   `PROCEDURE_TYPE`

Драйвери можуть повідомляти додаткові стовпці.

Результирующий набор упорядочивается по`PROCEDURE_CAT` `PROCEDURE_SCHEMA`и`PROCEDURE_NAME`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | До цієї версії функцію можна було викликати лише з одним чи чотирма аргументами. |

### Приклади

**Приклад #1 Перелік процедур бази даних, що зберігаються**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$procedures = odbc_procedures($conn, $catalog, $schema, '%');
while (($row = odbc_fetch_array($procedures))) {
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
    [NUM_INPUT_PARAMS] => -1
    [NUM_OUTPUT_PARAMS] => -1
    [NUM_RESULT_SETS] => -1
    [REMARKS] =>
    [PROCEDURE_TYPE] => 2
)
```

### Дивіться також

-   [odbc\_procedurecolumns()](function.odbc-procedurecolumns.md) \- Отримує інформацію про параметри процедур
-   [odbc\_tables()](function.odbc-tables.md) \- Отримує список імен таблиць, що зберігаються у певному джерелі даних
