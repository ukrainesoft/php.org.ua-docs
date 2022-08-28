Копіює дані з таблиці до масиву

-   [« pg\_copy\_from](function.pg-copy-from.html)
    
-   [pg\_dbname »](function.pg-dbname.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Копіює дані з таблиці до масиву
    

# пгcopyто

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгcopyto — Копіює дані з таблиці до масиву

### Опис

```methodsynopsis
pg_copy_to(    PgSql\Connection $connection,    string $table_name,    string $separator = "\t",    string $null_as = "\\\\N"): array|false
```

**пгcopyto()** копіює дані з таблиці до масиву. Для отримання записів посилає серверу команду SQL `COPY TO`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

`table_name`

Ім'я таблиці, з якої дані копіюються в масив `rows`

`separator`

Символ-розділювач, що відокремлює значення полів в елементах масиву `rows`. За замовчуванням `\t`

`null_as`

Цей параметр відповідає за те, як значення SQL `NULL` будуть представлені в масиві `rows`. За замовчуванням `\\N` `"\\\\N"`

### Значення, що повертаються

Масив (array), в якому кожен елемент - рядок, отриманий за допомогою `COPY` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгcopyto()****

```php
<?php
   $db = pg_connect("dbname=publisher") or die("Невозможно подключиться");

   $rows = pg_copy_to($db, $table_name);

   pg_query($db, "DELETE FROM $table_name");

   pg_copy_from($db, $table_name, $rows);
?>
```

### Дивіться також

-   [pg\_copy\_from()](function.pg-copy-from.html) - Вставляє записи з масиву до таблиці