---
navigation:
  - function.odbc-prepare.md: « odbc\_prepare
  - function.odbc-procedurecolumns.md: odbc\_procedurecolumns »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_primarykeys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_primarykeys

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_primarykeys — Отримує первинні ключі таблиці

### Опис

```methodsynopsis
odbc_primarykeys(    resource $odbc,    ?string $catalog,    string $schema,    string $table): resource|false
```

Повертає ідентифікатор результату, який можна використовувати для отримання імен шпальт, що становлять первинний ключ таблиці.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2).

`table`

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або \*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `COLUMN_NAME`
-   `KEY_SEQ`
-   `PK_NAME`

Драйвери можуть повідомляти додаткові стовпці.

Результирующий набор упорядочивается по`TABLE_CAT` `TABLE_SCHEM` `TABLE_NAME`и`KEY_SEQ`

### Приклади

**Приклад #1 Перелік первинних ключів шпальти**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$primarykeys = odbc_primarykeys($conn, 'TutorialDB', 'dbo', 'TEST');
while (($row = odbc_fetch_array($primarykeys))) {
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
    [KEY_SEQ] => 1
    [PK_NAME] => PK__TEST__3213E83FE141F843
)
```

### Дивіться також

-   [odbc\_tables()](function.odbc-tables.md) \- Отримує список імен таблиць, що зберігаються у певному джерелі даних
-   [odbc\_foreignkeys()](function.odbc-foreignkeys.md) \- Повертає список зовнішніх ключів
