---
navigation:
  - function.pg-copy-from.md: « pgcopyfrom
  - function.pg-dbname.md: пгdbname »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгcopyто
---
# пгcopyто

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгcopyto — Копіює дані з таблиці до масиву

### Опис

```methodsynopsis
pg_copy_to(    PgSql\Connection $connection,    string $table_name,    string $separator = "\t",    string $null_as = "\\\\N"): array|false
```

**пгcopyto()** копіює дані з таблиці до масиву. Для отримання записів посилає серверу команду SQL `COPY TO`

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

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
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгcopyto()****

```php
<?php
   $db = pg_connect("dbname=publisher") or die("Невозможно подключиться");

   $rows = pg_copy_to($db, $table_name);

   pg_query($db, "DELETE FROM $table_name");

   pg_copy_from($db, $table_name, $rows);
?>
```

### Дивіться також

-   [пгcopyfrom()](function.pg-copy-from.md) - Вставляє записи з масиву до таблиці
