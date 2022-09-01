---
navigation:
  - function.pg-connection-status.html: « pgconnectionstatus
  - function.pg-convert.html: пгconvert »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгconsumeinput
---
# пгconsumeinput

(PHP 5> = 5.6.0, PHP 7, PHP 8)

пгconsumeinput — Читає вступні дані на з'єднанні

### Опис

```methodsynopsis
pg_consume_input(PgSql\Connection $connection): bool
```

**пгconsumeinput()** приймає будь-які вхідні дані, які очікують на читання з сервера бази даних.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

### Значення, що повертаються

\*\*`true`\*\*якщо помилки не виникло, або **`false`**, якщо сталася помилка. Зверніть увагу, що **`true`** не обов'язково вказує, що вхідні дані очікували на читання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
