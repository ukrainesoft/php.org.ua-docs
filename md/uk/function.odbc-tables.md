---
navigation:
  - function.odbc-tableprivileges.md: « odbc\_tableprivileges
  - book.pdo.md: PDO »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_tables
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_tables

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_tables — Отримує список імен таблиць, що зберігаються у певному джерелі даних

### Опис

```methodsynopsis
odbc_tables(    resource $odbc,    ?string $catalog = null,    ?string $schema = null,    ?string $table = null,    ?string $types = null): resource|false
```

Перелічує всі таблиці у запрошеному діапазоні.

Для підтримки перерахування кваліфікаторів, власників та типів таблиць доступна наступна спеціальна семантика для `catalog` `schema` `table`и`table_type` :

-   Если значение`catalog`дорівнює символу відсотка (%), а`schema`и`table`є порожніми рядками, то результуючий набір міститиме список допустимих кваліфікаторів для джерела даних (усі стовпці, крім стовпця TABLE\_QUALIFIER, містять NULL).
-   Если значение`schema`дорівнює символу відсотка (%), а`catalog`и`table`є порожніми рядками, то результуючий набір міститиме список допустимих власників для джерела даних (усі стовпці, крім стовпця TABLE\_OWNER, містять NULL).
-   Если значение`table_type`дорівнює символу відсотка (%), а`catalog` `schema`и`table`є порожніми рядками, то результуючий набір міститиме список допустимих типів таблиць для джерела даних. (Всі стовпці, крім стовпця TABLE\_TYPE, містять NULL).

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2). Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`table`

Ім'я таблиці. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`types`

Якщо параметр `table_type` не є порожнім рядком, то він повинен містити список значень, розділених комами, для типів, що цікавлять; кожне значення може бути укладено в одинарні лапки (`'`) або не укладено в лапки. Наприклад, `'TABLE','VIEW'`или`TABLE, VIEW`. Якщо джерело даних не підтримує зазначений тип таблиці, **odbc\_tables()** не поверне жодних результатів цього типу.

### Значення, що повертаються

Возвращает идентификатор результата ODBC, содержащий информацию или\*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `TABLE_TYPE`
-   `REMARKS`

Драйвери можуть повідомляти додаткові стовпці.

Результирующий набор упорядочивается по`TABLE_TYPE` `TABLE_CAT` `TABLE_SCHEM`и`TABLE_NAME`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `schema` `table`и`types` тепер можуть набувати значення null. |

### Приклади

**Приклад #1 Перелік таблиць у каталозі**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$tables = odbc_tables($conn, 'SalesOrders', 'dbo', '%', 'TABLE');
while (($row = odbc_fetch_array($tables))) {
    print_r($row);
    break; // последующие строки опущены для краткости
}
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [odbc\_tableprivileges()](function.odbc-tableprivileges.md) \- Перераховує таблиці та привілеї, пов'язані з кожною таблицею
-   [odbc\_columns()](function.odbc-columns.md) \- перераховує імена стовпців у зазначених таблицях
-   [odbc\_specialcolumns()](function.odbc-specialcolumns.md) \- Витягує особливі стовпці
-   [odbc\_statistics()](function.odbc-statistics.md) \- Отримує статистику про таблицю
-   [odbc\_procedures()](function.odbc-procedures.md) \- Отримує список процедур, що зберігаються у певному джерелі даних
