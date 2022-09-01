---
navigation:
  - function.pg-set-error-verbosity.html: « pgseterrorverbosity
  - function.pg-trace.html: пгtrace »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгsocket
---
# пгsocket

(PHP 5> = 5.6.0, PHP 7, PHP 8)

пгsocket — Отримати дескриптор тільки для читання на сокет, що лежить в основі з'єднання PostgreSQL

### Опис

```methodsynopsis
pg_socket(PgSql\Connection $connection): resource|false
```

**пгsocket()** повертає ресурс (resource) лише читання, відповідний сокету, лежачому основу даного з'єднання PostgreSQL.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

### Значення, що повертаються

Ресурс сокету у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
