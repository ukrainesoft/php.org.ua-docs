Виведення великого об'єкта у файл

-   [« pg\_lo\_create](function.pg-lo-create.html)
    
-   [pg\_lo\_import »](function.pg-lo-import.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Виведення великого об'єкта у файл
    

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

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

`pathname`

Повний шлях та ім'я файлу у клієнтській файловій системі для запису даних великого об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_lo\_import()](function.pg-lo-import.html) - Імпорт великого об'єкта з файлу