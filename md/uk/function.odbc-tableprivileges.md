Перелічує таблиці та привілеї, пов'язані з кожною таблицею

-   [« odbcstatistics](function.odbc-statistics.html)
    
-   [odbctables »](function.odbc-tables.html)
    
-   [PHP Manual](index.md)
    
-   [Функции ODBC](ref.uodbc.md)
    
-   Перелічує таблиці та привілеї, пов'язані з кожною таблицею
    

# odbctableprivileges

(PHP 4, PHP 5, PHP 7, PHP 8)

odbctableprivileges — Перераховує таблиці та привілеї, пов'язані з кожною таблицею

### Опис

```methodsynopsis
odbc_tableprivileges(    resource $odbc,    ?string $catalog,    string $schema,    string $table): resource|false
```

Перелічує таблиці у запитаному діапазоні та привілеї, пов'язані з кожною таблицею.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.html)

`catalog`

Каталог ('qualifier' мовою ODBC 2).

`schema`

Схема ('owner' мовою ODBC 2). Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

`table`

Ім'я таблиці. Цей параметр приймає такі шаблони пошуку: `%` відповідний нулю або більше символів, та `_` відповідний рівно одному символу.

### Значення, що повертаються

Ідентифікатор результату ODBC або **`false`** у разі виникнення помилки.

У результуючому наборі є такі стовпці:

-   `TABLE_CAT`
-   `TABLE_SCHEM`
-   `TABLE_NAME`
-   `GRANTOR`
-   `GRANTEE`
-   `PRIVILEGE`
-   `IS_GRANTABLE`

Драйвери можуть повідомляти додаткові стовпці.

Результуючий набір впорядковується за `TABLE_CAT` `TABLE_SCHEM` `TABLE_NAME` `PRIVILEGE` і `GRANTEE`

### Приклади

**Приклад #1 Перелік привілеїв таблиці**

```php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$privileges = odbc_tableprivileges($conn, 'SalesOrders', 'dbo', 'Orders');
while (($row = odbc_fetch_array($privileges))) {
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
    [GRANTOR] => dbo
    [GRANTEE] => dbo
    [PRIVILEGE] => DELETE
    [IS_GRANTABLE] => YES
)
```

### Дивіться також

-   [odbctables()](function.odbc-tables.html) - Отримує список імен таблиць, що зберігаються у певному джерелі даних