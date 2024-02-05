---
navigation:
  - function.pg-copy-from.md: « pg\_copy\_from
  - function.pg-dbname.md: pg\_dbname »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_copy\_to
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_copy\_to

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_copy\_to — Копіює дані з таблиці до масиву

### Опис

```methodsynopsis
pg_copy_to(    PgSql\Connection $connection,    string $table_name,    string $separator = "\t",    string $null_as = "\\\\N"): array|false
```

**pg\_copy\_to()** копіює дані з таблиці до масиву. Для отримання записів посилає серверу команду SQL `COPY TO`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`table_name`

Ім'я таблиці, з якої дані копіюються в масив `rows`

`separator`

Символ-розділювач, що відокремлює значення полів в елементах масиву `rows`По умолчанию`\t`

`null_as`

Цей параметр відповідає за те, як значення SQL `NULL` будуть представлені в масиві `rows`По умолчанию`\\N` `"\\\\N"`

### Значення, що повертаються

Масив (array), в якому кожен елемент - рядок, отриманий за допомогою `COPY`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_copy\_to()\*\*\*\*

```php
<?php
   $db = pg_connect("dbname=publisher") or die("Невозможно подключиться");

   $rows = pg_copy_to($db, $table_name);

   pg_query($db, "DELETE FROM $table_name");

   pg_copy_from($db, $table_name, $rows);
?>
```

### Дивіться також

-   [pg\_copy\_from()](function.pg-copy-from.md) \- Вставляє записи з масиву до таблиці
