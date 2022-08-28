Повертає ім'я хоста, що відповідає підключенню

-   [« pg\_get\_result](function.pg-get-result.html)
    
-   [pg\_insert »](function.pg-insert.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає ім'я хоста, що відповідає підключенню
    

# пгhost

(PHP 4, PHP 5, PHP 7, PHP 8)

пгhost — Повертає ім'я хоста, що відповідає підключенню

### Опис

```methodsynopsis
pg_host(?PgSql\Connection $connection = null): string
```

**пгhost()** повертає ім'я хоста, з яким встановлено задане з'єднання PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить ім'я підключеного через `connection` хоста, або порожній рядок у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `connection` тепер допускає значення null.                                                                                                                       |

### Приклади

**Приклад #1 Приклад використання **пгhost()****

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   print "Успешно подключились к : " . pg_host($pgsql_conn) . "<br/>\n";
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.html) - Відкриває з'єднання з базою даних PostgreSQL
-   [pg\_pconnect()](function.pg-pconnect.html) - Відкриває постійне з'єднання із сервером PostgreSQL