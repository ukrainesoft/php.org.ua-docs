Отримання параметрів з'єднання з сервером баз даних

-   [« pg\_num\_rows](function.pg-num-rows.html)
    
-   [pg\_parameter\_status »](function.pg-parameter-status.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Отримання параметрів з'єднання з сервером баз даних
    

# пгoptions

(PHP 4, PHP 5, PHP 7, PHP 8)

пгoptions — Отримання параметрів з'єднання з сервером баз даних

### Опис

```methodsynopsis
pg_options(?PgSql\Connection $connection = null): string
```

**пгoptions()** повертає рядок, що містить параметри з'єднання PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить параметри з'єднання `connection`

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `connection` тепер допускає значення null.                                                                                                                       |

### Приклади

**Приклад #1 Приклад використання **пгoptions()****

```php
<?php
   $pgsql_conn = pg_connect("dbname=mark host=localhost");
   echo pg_options($pgsql_conn);
?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.html) - Відкриває з'єднання з базою даних PostgreSQL