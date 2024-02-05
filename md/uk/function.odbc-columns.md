---
navigation:
  - function.odbc-columnprivileges.md: « odbc\_columnprivileges
  - function.odbc-commit.md: odbc\_commit »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_columns
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_columns

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_columns — Перелік імен стовпців у вказаних таблицях

### Опис

```methodsynopsis
odbc_columns(    resource $odbc,    ?string $catalog = null,    ?string $schema = null,    ?string $table = null,    ?string $column = null): resource|false
```

Перелічує всі стовпці у запрошеному діапазоні.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2). Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`table`

Ім'я таблиці. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`column`

Ім'я стовпця. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або \*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `COLUMN_NAME`
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

Результирующий набор упорядочивается по`TABLE_CAT` `TABLE_SCHEM` `TABLE_NAME`и`ORDINAL_POSITION`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `schema` `table`и`column` тепер допускають значення null. |

### Приклади

**Приклад #1 Перелік стовпців таблиці**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$columns = odbc_columns($conn, 'TutorialDB', 'dbo', 'test', '%');
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
    [TABLE_CAT] => TutorialDB
    [TABLE_SCHEM] => dbo
    [TABLE_NAME] => TEST
    [COLUMN_NAME] => id
    [DATA_TYPE] => 4
    [TYPE_NAME] => int
    [COLUMN_SIZE] => 10
    [BUFFER_LENGTH] => 4
    [DECIMAL_DIGITS] => 0
    [NUM_PREC_RADIX] => 10
    [NULLABLE] => 0
    [REMARKS] =>
    [COLUMN_DEF] =>
    [SQL_DATA_TYPE] => 4
    [SQL_DATETIME_SUB] =>
    [CHAR_OCTET_LENGTH] =>
    [ORDINAL_POSITION] => 1
    [IS_NULLABLE] => NO
)
```

### Дивіться також

-   [odbc\_columnprivileges()](function.odbc-columnprivileges.md) \- Перераховує стовпці та пов'язані привілеї для даної таблиці
-   [odbc\_procedurecolumns()](function.odbc-procedurecolumns.md) \- Отримує інформацію про параметри процедур
