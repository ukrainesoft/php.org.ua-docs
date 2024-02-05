---
navigation:
  - function.pg-last-oid.md: « pg\_last\_oid
  - function.pg-lo-create.md: pg\_lo\_create »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_close

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_close — Закриває великий об'єкт

### Опис

```methodsynopsis
pg_lo_close(PgSql\Lob $lob): bool
```

**pg\_lo\_close()** закриває великий об'єкт.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_loclose()**

### Список параметрів

`lob`

An[PgSql\\Lob](class.pgsql-lob.md)instance, returned by[pg\_lo\_open()](function.pg-lo-open.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_lo\_close()\*\*\*\*

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

-   [pg\_lo\_open()](function.pg-lo-open.md) \- Відкриває великий об'єкт бази даних
-   [pg\_lo\_create()](function.pg-lo-create.md) \- Створює великий об'єкт
-   [pg\_lo\_import()](function.pg-lo-import.md) \- Імпорт великого об'єкта з файлу
