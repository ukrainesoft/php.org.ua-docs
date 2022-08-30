Видалення великого об'єкту

-   [« pgлоtruncate](function.pg-lo-truncate.html)
    
-   [пглоwrite »](function.pg-lo-write.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Видалення великого об'єкту
    

# пглоunlink

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоunlink — Видалення великого об'єкта

### Опис

```methodsynopsis
pg_lo_unlink(PgSql\Connection $connection, int $oid): bool
```

**пглоunlink()** видаляє великий об'єкт із ідентифікатором `oid`

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгlounlink()**

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                       |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пглоunlink()****

```php
<?php
   // OID удаляемого объекта
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   pg_lo_unlink($database, $doc_oid);
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [пглоcreate()](function.pg-lo-create.html) - Створює великий об'єкт
-   [пглоimport()](function.pg-lo-import.html) - Імпорт великого об'єкта з файлу