---
navigation:
  - function.pg-unescape-bytea.md: « pg\_unescape\_bytea
  - function.pg-update.md: pg\_update »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_untrace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_untrace

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

pg\_untrace — Вимикає трасування з'єднання з PostgreSQL

### Опис

```methodsynopsis
pg_untrace(?PgSql\Connection $connection = null): true
```

Зупиняє трасування, запущене функцією [pg\_trace()](function.pg-trace.md)

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_untrace()\*\*\*\*

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   pg_trace('/tmp/trace.log', 'w', $pgsql_conn);
   pg_query("SELECT 1");
   pg_untrace($pgsql_conn);
   // Теперь трассировка взаимодействия с сервером отключена
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```

### Дивіться також

-   [pg\_trace()](function.pg-trace.md) \- Включає трасування підключення PostgreSQL
