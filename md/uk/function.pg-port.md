---
navigation:
  - function.pg-ping.md: « pg\_ping
  - function.pg-prepare.md: pg\_prepare »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_port
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_port

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_port — Повертає номер порту, який відповідає заданому з'єднанню

### Опис

```methodsynopsis
pg_port(?PgSql\Connection $connection = null): string
```

**pg\_port()** повертає номер порту, який відповідає заданому з'єднанню PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок (string), що відповідає номеру порту, або порожній рядок у разі помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_port()\*\*\*\*

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   print "Успешно соединено с портом : " . pg_port($pgsql_conn) . "<br/>\n";
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```
