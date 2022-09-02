---
navigation:
  - function.odbc-prepare.md: « odbcprepare
  - function.odbc-procedurecolumns.md: odbcprocedurecolumns »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcprimarykeys
---
# odbcprimarykeys

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcprimarykeys — Отримує первинні ключі таблиці

### Опис

```methodsynopsis
odbc_primarykeys(    resource $odbc,    ?string $catalog,    string $schema,    string $table): resource|false
```

Повертає ідентифікатор результату, який можна використовувати для отримання імен шпальт, що становлять первинний ключ таблиці.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.md)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2).

`table`

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або **`false`** у разі виникнення помилки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `COLUMN_NAME`
-   `KEY_SEQ`
-   `PK_NAME`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за `TABLE_CAT` `TABLE_SCHEM` `TABLE_NAME` і `KEY_SEQ`

### Приклади

**Приклад #1 Перелік первинних ключів шпальти**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$primarykeys = odbc_primarykeys($conn, 'TutorialDB', 'dbo', 'TEST');
while (($row = odbc_fetch_array($primarykeys))) {
    print_r($row);
    break; // последующие строки опущены для краткости
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [TABLE_CAT] => TutorialDB
    [TABLE_SCHEM] => dbo
    [TABLE_NAME] => TEST
    [COLUMN_NAME] => id
    [KEY_SEQ] => 1
    [PK_NAME] => PK__TEST__3213E83FE141F843
)
```

### Дивіться також

-   [odbctables()](function.odbc-tables.md) - Отримує список імен таблиць, що зберігаються у певному джерелі даних
-   [odbcforeignkeys()](function.odbc-foreignkeys.md) - Повертає список зовнішніх ключів
