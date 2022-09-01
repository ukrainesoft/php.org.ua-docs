---
navigation:
  - function.pg-close.html: « pgclose
  - function.pg-connect.html: пгconnect »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгconnectpoll
---
# пгconnectpoll

(PHP 5> = 5.6.0, PHP 7, PHP 8)

пгconnectpoll — Опитати статус спроби асинхронного з'єднання PostgreSQL.

### Опис

```methodsynopsis
pg_connect_poll(PgSql\Connection $connection): int
```

**пгconnectpoll()** опитує статус з'єднання PostgreSQL, створеного викликом функції [пгconnect()](function.pg-connect.md) з параметром **`PGSQL_CONNECT_ASYNC`**

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`PGSQL_POLLING_FAILED`** **`PGSQL_POLLING_READING`** **`PGSQL_POLLING_WRITING`** **`PGSQL_POLLING_OK`** або **`PGSQL_POLLING_ACTIVE`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
