---
navigation:
  - function.pg-transaction-status.md: « pgtransactionstatus
  - function.pg-unescape-bytea.md: пгunescapebytea »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгtty
---
# пгtty

(PHP 4, PHP 5, PHP 7, PHP 8)

пгtty - Повертає ім'я терміналу TTY, пов'язане зі з'єднанням

### Опис

```methodsynopsis
pg_tty(?PgSql\Connection $connection = null): string
```

**пгtty()** повертає ім'я терміналу, пов'язаного з екземпляром `connection`, на який виводиться налагоджувальна інформація.

> **Зауваження**
> 
> **пгtty()** застаріла, але залишена для зворотної сумісності.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Ім'я TTY для підключення `connection` у вигляді рядка (string).

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгtty()****

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   print "TTY отладки сервера: " . pg_tty($pgsql_conn) . "<br/>\n";
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```
