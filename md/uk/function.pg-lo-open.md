Відкриває великий об'єкт бази даних

-   [« pg\_lo\_import](function.pg-lo-import.html)
    
-   [pg\_lo\_read\_all »](function.pg-lo-read-all.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Відкриває великий об'єкт бази даних
    

# пглоopen

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоopen — Відкриває великий об'єкт бази даних

### Опис

```methodsynopsis
pg_lo_open(PgSql\Connection $connection, int $oid, string $mode): PgSql\Lob|false
```

**пглоopen()** відкриває великий об'єкт бази даних та повертає екземпляр [PgSql\\Lob](class.pgsql-lob.html)

**Увага**

Не слід закривати з'єднання з базою даних до завершення роботи з екземпляром [PgSql\\Lob](class.pgsql-lob.html)

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгloopen()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

`mode`

Режим доступу до об'єкта. Можливі значення: "r" - лише для читання, "w" - лише для запису, "rw" - для читання та запису.

### Значення, що повертаються

Екземпляр [PgSql\\Lob](class.pgsql-lob.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Повертає екземпляр [PgSql\\Lob](class.pgsql-lob.html); раніше повертався ресурс ([resource](language.types.resource.html)                                        |
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пглоopen()****

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

-   [pg\_lo\_close()](function.pg-lo-close.html) - Закриває великий об'єкт
-   [pg\_lo\_create()](function.pg-lo-create.html) - Створює великий об'єкт