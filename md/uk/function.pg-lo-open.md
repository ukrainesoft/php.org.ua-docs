Відкриває великий об'єкт бази даних

-   [« pgлоimport](function.pg-lo-import.html)
    
-   [пглоreadall »](function.pg-lo-read-all.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Відкриває великий об'єкт бази даних
    

# пглоopen

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоopen — Відкриває великий об'єкт бази даних

### Опис

```methodsynopsis
pg_lo_open(PgSql\Connection $connection, int $oid, string $mode): PgSql\Lob|false
```

**пглоopen()** відкриває великий об'єкт бази даних та повертає екземпляр [PgSqlLob](class.pgsql-lob.html)

**Увага**

Не слід закривати з'єднання з базою даних до завершення роботи з екземпляром [PgSqlLob](class.pgsql-lob.html)

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгloopen()**

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

`mode`

Режим доступу до об'єкта. Можливі значення: "r" - лише для читання, "w" - лише для запису, "rw" - для читання та запису.

### Значення, що повертаються

Екземпляр [PgSqlLob](class.pgsql-lob.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PgSqlLob](class.pgsql-lob.html); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [пглоclose()](function.pg-lo-close.html) - Закриває великий об'єкт
-   [пглоcreate()](function.pg-lo-create.html) - Створює великий об'єкт