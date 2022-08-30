Вимикає трасування з'єднання з PostgreSQL

-   [« pgunescapebytea](function.pg-unescape-bytea.html)
    
-   [пгupdate »](function.pg-update.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Вимикає трасування з'єднання з PostgreSQL
    

# пгuntrace

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

пгuntrace — Вимикає трасування з'єднання з PostgreSQL

### Опис

```methodsynopsis
pg_untrace(?PgSql\Connection $connection = null): bool
```

Зупиняє трасування, запущене функцією [пгtrace()](function.pg-trace.html)

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Описание                                                                                                                                                       |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `connection` тепер допускає значення null.                                                                                                                     |

### Приклади

**Приклад #1 Приклад використання **пгuntrace()****

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   pg_trace('/tmp/trace.log', 'w', $pgsql_conn);
   pg_query("SELECT 1");
   pg_untrace($pgsql_conn);
   // Теперь трассировка взаимодействия с сервером отключена
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```

### Дивіться також

-   [пгtrace()](function.pg-trace.html) - Включає трасування підключення PostgreSQL