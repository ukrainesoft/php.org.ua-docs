---
navigation:
  - function.odbc-statistics.md: « odbc\_statistics
  - function.odbc-tables.md: odbc\_tables »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_tableprivileges
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_tableprivileges

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_tableprivileges — Перелічує таблиці та привілеї, пов'язані з кожною таблицею

### Опис

```methodsynopsis
odbc_tableprivileges(    resource $odbc,    ?string $catalog,    string $schema,    string $table): resource|false
```

Перелічує таблиці у запитаному діапазоні та привілеї, пов'язані з кожною таблицею.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2). Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`table`

Ім'я таблиці. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

### Значення, що повертаються

Идентификатор результата ODBC или\*\*`false`\*\*в случае возникновения ошибки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `GRANTOR`
-   `GRANTEE`
-   `PRIVILEGE`
-   `IS_GRANTABLE`

Драйвери можуть повідомляти додаткові стовпці.

Результирующий набор упорядочивается по`TABLE_CAT` `TABLE_SCHEM` `TABLE_NAME` `PRIVILEGE`и`GRANTEE`

### Приклади

**Приклад #1 Перелік привілеїв таблиці**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$privileges = odbc_tableprivileges($conn, 'SalesOrders', 'dbo', 'Orders');
while (($row = odbc_fetch_array($privileges))) {
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
    [GRANTOR] => dbo
    [GRANTEE] => dbo
    [PRIVILEGE] => DELETE
    [IS_GRANTABLE] => YES
)
```

### Дивіться також

-   [odbc\_tables()](function.odbc-tables.md) \- Отримує список імен таблиць, що зберігаються у певному джерелі даних
