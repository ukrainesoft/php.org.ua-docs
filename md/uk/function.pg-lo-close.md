Закриває великий об'єкт

-   [« pg\_last\_oid](function.pg-last-oid.html)
    
-   [pg\_lo\_create »](function.pg-lo-create.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Закриває великий об'єкт
    

# пглоclose

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоclose — Закриває великий об'єкт

### Опис

```methodsynopsis
pg_lo_close(PgSql\Lob $lob): bool
```

**пглоclose()** закриває великий об'єкт.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгloclose()**

### Список параметрів

`lob`

Ан [PgSql\\Lob](class.pgsql-lob.html) instance, returned by [pg\_lo\_open()](function.pg-lo-open.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пглоclose()****

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

### Дивіться також

-   [pg\_lo\_open()](function.pg-lo-open.html) - Відкриває великий об'єкт бази даних
-   [pg\_lo\_create()](function.pg-lo-create.html) - Створює великий об'єкт
-   [pg\_lo\_import()](function.pg-lo-import.html) - Імпорт великого об'єкта з файлу