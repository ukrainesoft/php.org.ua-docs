Закриває великий об'єкт

-   [« pglastoid](function.pg-last-oid.html)
    
-   [пглоcreate »](function.pg-lo-create.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
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

Ан [PgSqlLob](class.pgsql-lob.html) instance, returned by [пглоopen()](function.pg-lo-open.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `lob` тепер чекає екземпляр [PgSqlLob](class.pgsql-lob.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [пглоopen()](function.pg-lo-open.html) - Відкриває великий об'єкт бази даних
-   [пглоcreate()](function.pg-lo-create.html) - Створює великий об'єкт
-   [пглоimport()](function.pg-lo-import.html) - Імпорт великого об'єкта з файлу