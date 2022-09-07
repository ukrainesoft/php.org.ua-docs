---
navigation:
  - function.pg-unescape-bytea.md: « pgunescapebytea
  - function.pg-update.md: пгupdate »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгuntrace
---
# пгuntrace

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

пгuntrace — Вимикає трасування з'єднання з PostgreSQL

### Опис

```methodsynopsis
pg_untrace(?PgSql\Connection $connection = null): bool
```

Зупиняє трасування, запущене функцією [пгtrace()](function.pg-trace.md)

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгuntrace()****

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

-   [пгtrace()](function.pg-trace.md) - Включає трасування підключення PostgreSQL
