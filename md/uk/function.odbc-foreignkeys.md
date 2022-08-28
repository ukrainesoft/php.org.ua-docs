Повертає список зовнішніх ключів

-   [« odbc\_field\_type](function.odbc-field-type.html)
    
-   [odbc\_free\_result »](function.odbc-free-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає список зовнішніх ключів
    

# odbcforeignkeys

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcforeignkeys — Повертає список зовнішніх ключів

### Опис

```methodsynopsis
odbc_foreignkeys(    resource $odbc,    ?string $pk_catalog,    string $pk_schema,    string $pk_table,    string $fk_catalog,    string $fk_schema,    string $fk_table): resource|false
```

Повертає список зовнішніх ключів у таблиці або список зовнішніх ключів в інших таблицях, які посилаються на первинний ключ у зазначеній таблиці.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.html)

`fk_catalog`

Каталог ('кваліфікатор' мовою ODBC 2) таблиці з первинним ключем.

`pk_schema`

Схема ('власник' мовою ODBC 2) таблиці з первинним ключем.

`pk_table`

Таблиця із первинним ключем.

`pk_catalog`

Каталог ('кваліфікатор' мовою ODBC 2) таблиці із зовнішнім ключем.

`fk_schema`

Схема ('власник' мовою ODBC 2) таблиці із зовнішнім ключем.

`fk_table`

Таблиця із зовнішнім ключем.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC або **`false`** у разі виникнення помилки.

У результуючому наборі є такі стовпці:

-   `PKTABLE_CAT`
-   `PKTABLE_SCHEM`
-   `PKTABLE_NAME`
-   `PKCOLUMN_NAME`
-   `FKTABLE_CAT`
-   `FKTABLE_SCHEM`
-   `FKTABLE_NAME`
-   `FKCOLUMN_NAME`
-   `KEY_SEQ`
-   `UPDATE_RULE`
-   `DELETE_RULE`
-   `FK_NAME`
-   `PK_NAME`
-   `DEFERRABILITY`

Драйвери можуть повідомляти додаткові стовпці.

Якщо запитуються зовнішні ключі, пов'язані з первинним ключем, результуючий набір впорядковується `FKTABLE_CAT` `FKTABLE_SCHEM` `FKTABLE_NAME` і `KEY_SEQ`. Якщо запитуються первинні ключі, пов'язані із зовнішнім ключем, результуючий набір впорядковується за `PKTABLE_CAT` `PKTABLE_SCHEM` `PKTABLE_NAME` і `KEY_SEQ`

Якщо `pk_table` містить ім'я таблиці, **odbcforeignkeys()** повертає результуючий набір, що містить первинний ключ зазначеної таблиці та всі зовнішні ключі, які посилаються на нього.

Якщо `fk_table` містить ім'я таблиці, **odbcforeignkeys()** повертає результуючий набір, що містить усі зовнішні ключі у зазначеній таблиці та первинні ключі (в інших таблицях), на які вони посилаються.

Якщо і `pk_table` і `fk_table` містять імена таблиць, **odbcforeignkeys()** повертає зовнішні ключі в таблиці, вказаній у `fk_table`, які посилаються на первинний ключ таблиці, вказаної в `pk_table`. Ключ має бути один, не більше.

### Дивіться також

-   [odbc\_tables()](function.odbc-tables.html) - Отримує список імен таблиць, що зберігаються у певному джерелі даних
-   [odbc\_primarykeys()](function.odbc-primarykeys.html) - Отримує первинні ключі таблиці