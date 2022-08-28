Визначає ім'я бази даних

-   [« pg\_copy\_to](function.pg-copy-to.html)
    
-   [pg\_delete »](function.pg-delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Визначає ім'я бази даних
    

# пгdbname

(PHP 4, PHP 5, PHP 7, PHP 8)

пгdbname — Визначає ім'я бази даних

### Опис

```methodsynopsis
pg_dbname(?PgSql\Connection $connection = null): string
```

**пгdbname()** повертає ім'я бази даних, що відповідає екземпляру PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить ім'я бази даних, що відповідає ресурсу `connection`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгdbname()****

```php
<?php
  error_reporting(E_ALL);

  pg_connect("host=localhost port=5432 dbname=mary");
  echo pg_dbname(); // mary
?>
```