Отримання кодування клієнта.

-   [« pg\_cancel\_query](function.pg-cancel-query.html)
    
-   [pg\_close »](function.pg-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Отримання кодування клієнта.
    

# пгclientencoding

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

пгclientencoding — отримання кодування клієнта.

### Опис

```methodsynopsis
pg_client_encoding(?PgSql\Connection $connection = null): string
```

PostgreSQL підтримує автоматичне перетворення наборів символів між сервером та клієнтом для деяких кодувань . **пгclientencoding()** повертає клієнтське кодування у вигляді рядка, що є стандартним ідентифікатором кодування PostgreSQL.

> **Зауваження**
> 
> Для роботи функції потрібно PostgreSQL версії 7.0 або вищою. У випадку, якщо libpg скомпільована без підтримки багатобайтових кодувань, **пгclientencoding()** завжди повертає `SQL_ASCII`. Набір кодувань, що підтримуються, залежить від версії сервера БД і описаний в документації PostgreSQL.
> 
> Функція для дзвінка: **пгclientencoding()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Клієнтське кодування.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `connection` тепер допускає значення null.                                                                                                                       |

### Приклади

**Приклад #1 Приклад використання **пгclientencoding()****

```php
<?php
// Допустим, что $conn - соединение с базой данных, поддерживающей стандарт ISO-8859-1
$encoding = pg_client_encoding($conn);

echo "Кодировка клиента: ", $encoding, "\n";
?>
```

Результат виконання цього прикладу:

```
Кодировка клиента: ISO-8859-1
```

### Дивіться також

-   [pg\_set\_client\_encoding()](function.pg-set-client-encoding.html) - Встановлює клієнтське кодування