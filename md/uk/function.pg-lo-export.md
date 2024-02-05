---
navigation:
  - function.pg-lo-create.md: « pg\_lo\_create
  - function.pg-lo-import.md: pg\_lo\_import »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_export

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_export — Виведення великого об'єкта у файл

### Опис

```methodsynopsis
pg_lo_export(PgSql\Connection $connection = ?, int $oid, string $pathname): bool
```

**pg\_lo\_export()** вибирає великий об'єкт із бази даних та зберігає його дані локально у файловій системі.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_loexport()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

`pathname`

Повний шлях та ім'я файлу у клієнтській файловій системі для запису даних великого об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_lo\_export()\*\*\*\*

```php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_create($database);
   $handle = pg_lo_open($database, $oid, "w");
   pg_lo_write($handle, "large object data");
   pg_lo_close($handle);
   pg_lo_export($database, $oid, '/tmp/lob.dat');
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [pg\_lo\_import()](function.pg-lo-import.md) \- Імпорт великого об'єкта з файлу
