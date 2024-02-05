---
navigation:
  - function.pg-connection-status.md: « pg\_connection\_status
  - function.pg-convert.md: pg\_convert »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_consume\_input
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_consume\_input

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

pg\_consume\_input — Читає вступні дані на з'єднанні

### Опис

```methodsynopsis
pg_consume_input(PgSql\Connection $connection): bool
```

**pg\_consume\_input()** приймає будь-які вхідні дані, які очікують на читання з сервера бази даних.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

**`true`**якщо помилки не виникло, або **`false`**, если произошла ошибка. Обратите внимание, что**`true`** не обов'язково вказує, що вхідні дані очікували на читання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
