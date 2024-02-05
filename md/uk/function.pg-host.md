---
navigation:
  - function.pg-get-result.md: « pg\_get\_result
  - function.pg-insert.md: pg\_insert »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_host
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_host

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_host — Повертає ім'я хоста, що відповідає підключенню

### Опис

```methodsynopsis
pg_host(?PgSql\Connection $connection = null): string
```

**pg\_host()** повертає ім'я хоста, з яким встановлено задане з'єднання PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить ім'я підключеного через `connection`хоста, либо пустая строка в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** pg\_host()\*\*\*\*

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   print "Успешно подключились к : " . pg_host($pgsql_conn) . "<br/>\n";
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.md) \- Відкриває з'єднання з базою даних PostgreSQL
-   [pg\_pconnect()](function.pg-pconnect.md) \- Відкриває постійне з'єднання із сервером PostgreSQL
