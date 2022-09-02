---
navigation:
  - function.pg-lo-create.md: « pgлоcreate
  - function.pg-lo-import.md: пглоimport »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пглоexport
---
# пглоexport

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоexport — Виведення великого об'єкта у файл

### Опис

```methodsynopsis
pg_lo_export(PgSql\Connection $connection = ?, int $oid, string $pathname): bool
```

**пглоexport()** вибирає великий об'єкт із бази даних та зберігає його дані локально у файловій системі.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгloexport()**

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

`pathname`

Повний шлях та ім'я файлу у клієнтській файловій системі для запису даних великого об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пглоexport()****

```php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_create($database);
   $handle = pg_lo_open($database, $oid, "w");
   pg_lo_write($handle, "large object data");
   pg_lo_close($handle);
   pg_lo_export($database, $oid, '/tmp/lob.dat');
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [пглоimport()](function.pg-lo-import.md) - Імпорт великого об'єкта з файлу
