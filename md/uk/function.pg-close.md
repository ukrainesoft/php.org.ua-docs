Закриває з'єднання з базою даних PostgreSQL

-   [« pgclientencoding](function.pg-client-encoding.html)
    
-   [пгconnectpoll »](function.pg-connect-poll.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Закриває з'єднання з базою даних PostgreSQL
    

# пгclose

(PHP 4, PHP 5, PHP 7, PHP 8)

пгclose — Закриває з'єднання з базою даних PostgreSQL

### Опис

```methodsynopsis
pg_close(?PgSql\Connection $connection = null): bool
```

**пгclose()** закриває звичайне (непостійне) з'єднання з базою даних PostgreSQL, що відповідає екземпляру `connection`

> **Зауваження**
> 
> Використання **пгclose()**, зазвичай, необов'язково, оскільки непостійні з'єднання закриваються автоматично після завершення роботи скрипта.

Якщо зі з'єднанням працюють екземпляри [PgSqlLob](class.pgsql-lob.html), то перед закриттям з'єднання необхідно закрити всі екземпляри [PgSqlLob](class.pgsql-lob.html)

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

**Приклад #1 Приклад використання **пгclose()****

```php
<?php
$dbconn = pg_connect("host=localhost port=5432 dbname=mary")
   or die("Невозможно подключиться к БД");
echo "Успешно подключено к БД";
pg_close($dbconn);
?>
```

Результат виконання цього прикладу:

```
Успешно подключено к БД
```

### Дивіться також

-   [пгconnect()](function.pg-connect.html) - Відкриває з'єднання з базою даних PostgreSQL