Отримує статистику про таблицю

-   [« odbc\_specialcolumns](function.odbc-specialcolumns.html)
    
-   [odbc\_tableprivileges »](function.odbc-tableprivileges.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Отримує статистику про таблицю
    

# odbcstatistics

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcstatistics — Отримує статистику про таблицю

### Опис

```methodsynopsis
odbc_statistics(    resource $odbc,    ?string $catalog,    string $schema,    string $table,    int $unique,    int $accuracy): resource|false
```

Отримує статистику про таблицю та її індекси.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.html)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2).

`table`

Ім'я таблиці.

`unique`

Тип індексу. Одна з констант **`SQL_INDEX_UNIQUE`** або **`SQL_INDEX_ALL`**

`accuracy`

Одна з констант **`SQL_ENSURE`** або **`SQL_QUICK`**. Остання запитує у драйвера отримання `CARDINALITY` і `PAGES`тільки якщо вони легко доступні з сервера.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або **`false`** у разі виникнення помилки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `NON_UNIQUE`
-   `INDEX_QUALIFIER`
-   `INDEX_NAME`
-   `TYPE`
-   `ORDINAL_POSITION`
-   `COLUMN_NAME`
-   `ASC_OR_DESC`
-   `CARDINALITY`
-   `PAGES`
-   `FILTER_CONDITION`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за `NON_UNIQUE` `TYPE` `INDEX_QUALIFIER` `INDEX_NAME` і `ORDINAL_POSITION`

### Приклади

**Приклад #1 Висновок статистики про таблицю**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$statistics = odbc_statistics($conn, 'TutorialDB', 'dbo', 'TEST', SQL_INDEX_UNIQUE, SQL_QUICK);
while (($row = odbc_fetch_array($statistics))) {
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
    [NON_UNIQUE] =>
    [INDEX_QUALIFIER] =>
    [INDEX_NAME] =>
    [TYPE] => 0
    [ORDINAL_POSITION] =>
    [COLUMN_NAME] =>
    [ASC_OR_DESC] =>
    [CARDINALITY] => 15
    [PAGES] => 3
    [FILTER_CONDITION] =>
)
```

### Дивіться також

-   [odbc\_tables()](function.odbc-tables.html) - Отримує список імен таблиць, що зберігаються у певному джерелі даних