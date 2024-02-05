---
navigation:
  - function.pg-lo-close.md: « pg\_lo\_close
  - function.pg-lo-export.md: pg\_lo\_export »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_create

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_create — Створює великий об'єкт

### Опис

```methodsynopsis
pg_lo_create(PgSql\Connection $connection = ?, mixed $object_id = ?): int
```

```methodsynopsis
pg_lo_create(mixed $object_id): int
```

**pg\_lo\_create()** створює великий об'єкт та повертає його OID. Режими доступу PostgreSQL **`INV_READ`** **`INV_WRITE`**, и\*\*`INV_ARCHIVE`\*\* не підтримуються, об'єкт завжди створюється з доступом на читання та запис. Режим **`INV_ARCHIVE`** прибраний з PostgreSQL версій 6.3 та вище.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

Замість використання інтерфейсу великих об'єктів (який не має контролю доступу і дуже громіздкий сам по собі) користуйтеся полями PostgreSQL типу bytea для зберігання бінарних даних та функцією [pg\_escape\_bytea()](function.pg-escape-bytea.md) для їхнього екранування.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_locreate()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`object_id`

Если задан аргумент`object_id`, функція спробує створити об'єкт із цим ідентифікатором, інакше буде використано вільний ідентифікатор, призначений сервером. Цей аргумент ґрунтується на функціоналі, вперше реалізованому в PostgreSQL 8.1.

### Значення, що повертаються

OID великого об'єкта або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_create()\*\*\*\*

```php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_create($database);
   echo "$oid\n";
   $handle = pg_lo_open($database, $oid, "w");
   echo "$handle\n";
   pg_lo_write($handle, "large object data");
   pg_lo_close($handle);
   pg_query($database, "commit");
?>
```
