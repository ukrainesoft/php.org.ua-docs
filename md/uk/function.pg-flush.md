---
navigation:
  - function.pg-field-type.md: « pg\_field\_type
  - function.pg-free-result.md: pg\_free\_result »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_flush
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_flush

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

pg\_flush — Скинути дані вихідного запиту на з'єднанні

### Опис

```methodsynopsis
pg_flush(PgSql\Connection $connection): int|bool
```

**pg\_flush()** скидає будь-які дані вихідного запиту, що очікують надсилання на з'єднанні.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`true`**, якщо скидання було успішним або дані не очікували скидання, або , якщо частина очікуваних даних була скинута, однак залишилися ще \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
