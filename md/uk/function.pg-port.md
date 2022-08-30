Повертає номер порту, який відповідає заданому з'єднанню

-   [« pgping](function.pg-ping.html)
    
-   [пгprepare »](function.pg-prepare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає номер порту, який відповідає заданому з'єднанню
    

# пгport

(PHP 4, PHP 5, PHP 7, PHP 8)

пгport — Повертає номер порту, який відповідає заданому з'єднанню

### Опис

```methodsynopsis
pg_port(?PgSql\Connection $connection = null): string
```

**пгport()** повертає номер порту, який відповідає заданому з'єднанню PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок (string), що відповідає номеру порту, або порожній рядок у разі помилки.

### список змін

| Версия | Описание                                                                                                                                                       |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `connection` тепер допускає значення null.                                                                                                                     |

### Приклади

**Приклад #1 Приклад використання **пгport()****

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   print "Успешно соединено с портом : " . pg_port($pgsql_conn) . "<br/>\n";
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```