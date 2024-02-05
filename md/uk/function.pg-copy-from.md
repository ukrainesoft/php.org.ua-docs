---
navigation:
  - function.pg-convert.md: « pg\_convert
  - function.pg-copy-to.md: pg\_copy\_to »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_copy\_from
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_copy\_from

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_copy\_from — Вставляє записи з масиву до таблиці

### Опис

```methodsynopsis
pg_copy_from(    PgSql\Connection $connection,    string $table_name,    array $rows,    string $separator = "\t",    string $null_as = "\\\\N"): bool
```

\*\*pg\_copy\_from()\*\*вставляет записи в таблицу из массива`rows`. У ході виконання викликає SQL-команду `COPY FROM`для вставки записей.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`table_name`

Ім'я таблиці, в яку копіюються значення з `rows`

`rows`

Масив (array) даних для копіювання в `table_name`Каждое значение в`rows`становится строкой в`table_name`Каждое значение массива`rows` має бути рядком із роздільником, що містить значення для вставки у кожне поле таблиці. Значення мають закінчуватися символом перекладу рядка.

`separator`

Символ, що відокремлює значення один від одного в кожному елементі масиву `rows`По умолчанию`\t`

`null_as`

Визначає, яким чином значення SQL `NULL` представлені в масиві `rows`По умолчанию`\\N` `"\\\\N"`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_copy\_from()\*\*\*\*

```php
<?php
   $db = pg_connect("dbname=publisher") or die("Не удалось подключиться");

   $rows = pg_copy_to($db, $table_name);

   pg_query($db, "DELETE FROM $table_name");

   pg_copy_from($db, $table_name, $rows);
?>
```

### Дивіться також

-   [pg\_copy\_to()](function.pg-copy-to.md) \- Копіює дані з таблиці до масиву
