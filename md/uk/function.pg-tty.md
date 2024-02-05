---
navigation:
  - function.pg-transaction-status.md: « pg\_transaction\_status
  - function.pg-unescape-bytea.md: pg\_unescape\_bytea »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_tty
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_tty

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_tty - Повертає ім'я терміналу TTY, пов'язане зі з'єднанням

### Опис

```methodsynopsis
pg_tty(?PgSql\Connection $connection = null): string
```

**pg\_tty()** повертає ім'я терміналу, пов'язаного з екземпляром `connection`, на який виводиться налагоджувальна інформація.

> **Зауваження** :
> 
> **pg\_tty()** застаріла, але залишена для зворотної сумісності.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Имя TTY для подключения`connection` у вигляді рядка (string).

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** pg\_tty()\*\*\*\*

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   print "TTY отладки сервера: " . pg_tty($pgsql_conn) . "<br/>\n";
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```
