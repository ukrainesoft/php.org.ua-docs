---
navigation:
  - function.pg-lo-import.md: « pg\_lo\_import
  - function.pg-lo-read-all.md: pg\_lo\_read\_all »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_open

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_open — Відкриває великий об'єкт бази даних

### Опис

```methodsynopsis
pg_lo_open(PgSql\Connection $connection, int $oid, string $mode): PgSql\Lob|false
```

**pg\_lo\_open()** відкриває великий об'єкт бази даних та повертає екземпляр [PgSql\\Lob](class.pgsql-lob.md)

**Увага**

Не слід закривати з'єднання з базою даних до завершення роботи з екземпляром [PgSql\\Lob](class.pgsql-lob.md)

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_loopen()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

`mode`

Режим доступу до об'єкта. Можливі значення: "r" - лише для читання, "w" - лише для запису, "rw" - для читання та запису.

### Значення, що повертаються

Екземпляр [PgSql\\Lob](class.pgsql-lob.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_open()\*\*\*\*

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

### Дивіться також

-   [pg\_lo\_close()](function.pg-lo-close.md) \- Закриває великий об'єкт
-   [pg\_lo\_create()](function.pg-lo-create.md) \- Створює великий об'єкт
