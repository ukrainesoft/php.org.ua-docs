Опитати статус спроби з'єднання PostgreSQL.

-   [« pg\_close](function.pg-close.html)
    
-   [pg\_connect »](function.pg-connect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Опитати статус спроби з'єднання PostgreSQL.
    

# пгconnectpoll

(PHP 5> = 5.6.0, PHP 7, PHP 8)

пгconnectpoll — Опитати статус спроби асинхронного з'єднання PostgreSQL.

### Опис

```methodsynopsis
pg_connect_poll(PgSql\Connection $connection): int
```

**пгconnectpoll()** опитує статус з'єднання PostgreSQL, створеного викликом функції [pg\_connect()](function.pg-connect.html) з параметром **`PGSQL_CONNECT_ASYNC`**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

### Значення, що повертаються

Повертає **`PGSQL_POLLING_FAILED`** **`PGSQL_POLLING_READING`** **`PGSQL_POLLING_WRITING`** **`PGSQL_POLLING_OK`** або **`PGSQL_POLLING_ACTIVE`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |