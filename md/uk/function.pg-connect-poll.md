---
navigation:
  - function.pg-close.md: « pg\_close
  - function.pg-connect.md: pg\_connect »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_connect\_poll
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_connect\_poll

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

pg\_connect\_poll — Опитати статус спроби асинхронного з'єднання PostgreSQL.

### Опис

```methodsynopsis
pg_connect_poll(PgSql\Connection $connection): int
```

**pg\_connect\_poll()** опитує статус з'єднання PostgreSQL, створеного викликом функції [pg\_connect()](function.pg-connect.md)с параметром\*\*`PGSQL_CONNECT_ASYNC`\*\*

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`PGSQL_POLLING_FAILED`** **`PGSQL_POLLING_READING`** **`PGSQL_POLLING_WRITING`** **`PGSQL_POLLING_OK`** або **`PGSQL_POLLING_ACTIVE`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
