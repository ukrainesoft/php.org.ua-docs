---
navigation:
  - function.pg-convert.html: « pgconvert
  - function.pg-copy-to.html: пгcopyto »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгcopyfrom
---
# пгcopyfrom

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгcopyfrom — Вставляє записи з масиву до таблиці

### Опис

```methodsynopsis
pg_copy_from(    PgSql\Connection $connection,    string $table_name,    array $rows,    string $separator = "\t",    string $null_as = "\\\\N"): bool
```

**пгcopyfrom()** вставляє записи в таблицю з масиву `rows`. У ході виконання викликає SQL-команду `COPY FROM` для вставлення записів.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

`table_name`

Ім'я таблиці, в яку копіюються значення з `rows`

`rows`

Масив (array) даних для копіювання в `table_name`. Кожне значення у `rows` стає рядком у `table_name`. Кожне значення масиву `rows` має бути рядком із роздільником, що містить значення для вставки у кожне поле таблиці. Значення мають закінчуватися символом перекладу рядка.

`separator`

Символ, що відокремлює значення один від одного в кожному елементі масиву `rows`. За замовчуванням `\t`

`null_as`

Визначає, яким чином значення SQL `NULL` представлені в масиві `rows`. За замовчуванням `\\N` `"\\\\N"`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгcopyfrom()****

```php
<?php
   $db = pg_connect("dbname=publisher") or die("Не удалось подключиться");

   $rows = pg_copy_to($db, $table_name);

   pg_query($db, "DELETE FROM $table_name");

   pg_copy_from($db, $table_name, $rows);
?>
```

### Дивіться також

-   [пгcopyto()](function.pg-copy-to.html) - Копіює дані з таблиці до масиву
