---
navigation:
  - function.pg-lo-close.html: « pgлоclose
  - function.pg-lo-export.html: пглоexport »
  - index.html: PHP Manual
  - ref.pgsql.html: Функции PostgreSQL
title: пглоcreate
---
# пглоcreate

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоcreate — Створює великий об'єкт

### Опис

```methodsynopsis
pg_lo_create(PgSql\Connection $connection = ?, mixed $object_id = ?): int
```

```methodsynopsis
pg_lo_create(mixed $object_id): int
```

**пглоcreate()** створює великий об'єкт та повертає його OID. Режими доступу PostgreSQL **`INV_READ`** **`INV_WRITE`**, і **`INV_ARCHIVE`** не підтримуються, об'єкт завжди створюється з доступом на читання та запис. Режим **`INV_ARCHIVE`** прибраний з PostgreSQL версій 6.3 та вище.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

Замість використання інтерфейсу великих об'єктів (який не має контролю доступу і дуже громіздкий сам по собі) користуйтеся полями PostgreSQL типу bytea для зберігання бінарних даних та функцією [пгescapebytea()](function.pg-escape-bytea.html) для їхнього екранування.

> **Зауваження**
> 
> Колишня назва функції: **пгlocreate()**

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`object_id`

Якщо заданий аргумент `object_id`, функція спробує створити об'єкт із цим ідентифікатором, інакше буде використано вільний ідентифікатор, призначений сервером. Цей аргумент ґрунтується на функціоналі, вперше реалізованому в PostgreSQL 8.1.

### Значення, що повертаються

OID великого об'єкта або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пглоcreate()****

```php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_create($database);
   echo "$oid\n";
   $handle = pg_lo_open($database, $oid, "w");
   echo "$handle\n";
   pg_lo_write($handle, "large object data");
   pg_lo_close($handle);
   pg_query($database, "commit");
?>
```
