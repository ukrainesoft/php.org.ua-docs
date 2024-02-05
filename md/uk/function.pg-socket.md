---
navigation:
  - function.pg-set-error-verbosity.md: « pg\_set\_error\_verbosity
  - function.pg-trace.md: pg\_trace »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_socket
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_socket

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

pg\_socket — Отримати дескриптор тільки для читання на сокет, що лежить в основі з'єднання PostgreSQL

### Опис

```methodsynopsis
pg_socket(PgSql\Connection $connection): resource|false
```

**pg\_socket()** повертає ресурс (resource) лише читання, відповідний сокету, лежачому основу даного з'єднання PostgreSQL.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Ресурс сокету у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
