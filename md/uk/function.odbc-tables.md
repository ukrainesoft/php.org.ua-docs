---
navigation:
  - function.odbc-tableprivileges.html: « odbctableprivileges
  - book.pdo.md: PDO »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbctables
---
# odbctables

(PHP 4, PHP 5, PHP 7, PHP 8)

odbctables — Отримує список імен таблиць, що зберігаються у певному джерелі даних

### Опис

```methodsynopsis
odbc_tables(    resource $odbc,    ?string $catalog = null,    ?string $schema = null,    ?string $table = null,    ?string $types = null): resource|false
```

Перелічує всі таблиці у запрошеному діапазоні.

Для підтримки перерахування кваліфікаторів, власників та типів таблиць доступна наступна спеціальна семантика для `catalog` `schema` `table` і `table_type`

-   Якщо значення `catalog` дорівнює символу відсотка (%), а `schema` і `table` є порожніми рядками, то результуючий набір міститиме список допустимих кваліфікаторів для джерела даних (усі стовпці, крім стовпця TABLEQUALIFIER, містять NULL).
-   Якщо значення `schema` дорівнює символу відсотка (%), а `catalog` і `table` є порожніми рядками, то результуючий набір міститиме список допустимих власників для джерела даних (усі стовпці, крім стовпця TABLEOWNER, містять NULL).
-   Якщо значення `table_type` дорівнює символу відсотка (%), а `catalog` `schema` і `table` є порожніми рядками, то результуючий набір міститиме список допустимих типів таблиць для джерела даних. (Всі стовпці, крім стовпця TABLETYPE, містять NULL).

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbcconnect()](function.odbc-connect.html)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2). Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`table`

Ім'я таблиці. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`types`

Якщо параметр `table_type` не є порожнім рядком, то він повинен містити список значень, розділених комами, для типів, що цікавлять; кожне значення може бути укладено в одинарні лапки (`'`) або не укладено в лапки. Наприклад, `'TABLE','VIEW'` або `TABLE, VIEW`. Якщо джерело даних не підтримує зазначений тип таблиці, **odbctables()** не поверне жодних результатів цього типу.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC, який містить інформацію або **`false`** у разі виникнення помилки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `TABLE_TYPE`
-   `REMARKS`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за `TABLE_TYPE` `TABLE_CAT` `TABLE_SCHEM` і `TABLE_NAME`

### список змін

| Версия | Описание |
| --- | --- |
|  | `schema` `table` і `types` тепер можуть набувати значення null. |

### Приклади

**Приклад #1 Перелік таблиць у каталозі**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$tables = odbc_tables($conn, 'SalesOrders', 'dbo', '%', 'TABLE');
while (($row = odbc_fetch_array($tables))) {
    print_r($row);
    break; // последующие строки опущены для краткости
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [TABLE_CAT] => SalesOrders
    [TABLE_SCHEM] => dbo
    [TABLE_NAME] => Orders
    [TABLE_TYPE] => TABLE
    [REMARKS] =>
)
```

### Дивіться також

-   [odbctableprivileges()](function.odbc-tableprivileges.html) - Перераховує таблиці та привілеї, пов'язані з кожною таблицею
-   [odbccolumns()](function.odbc-columns.html) - перераховує імена стовпців у зазначених таблицях
-   [odbcspecialcolumns()](function.odbc-specialcolumns.html) - Витягує особливі стовпці
-   [odbcstatistics()](function.odbc-statistics.html) - Отримує статистику про таблицю
-   [odbcprocedures()](function.odbc-procedures.html) - Отримує список процедур, що зберігаються у певному джерелі даних
