Отримує первинні ключі таблиці

-   [« odbc\_prepare](function.odbc-prepare.html)
    
-   [odbc\_procedurecolumns »](function.odbc-procedurecolumns.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Отримує первинні ключі таблиці
    

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

Ідентифікатор з'єднання ODBC, див. [odbc\_connect()](function.odbc-connect.html)

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

-   [odbc\_tables()](function.odbc-tables.html) - Отримує список імен таблиць, що зберігаються у певному джерелі даних
-   [odbc\_foreignkeys()](function.odbc-foreignkeys.html) - Повертає список зовнішніх ключів