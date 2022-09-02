---
navigation:
  - function.pg-get-result.md: « pggetresult
  - function.pg-insert.md: пгinsert »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгhost
---
# пгhost

(PHP 4, PHP 5, PHP 7, PHP 8)

пгhost — Повертає ім'я хоста, що відповідає підключенню

### Опис

```methodsynopsis
pg_host(?PgSql\Connection $connection = null): string
```

**пгhost()** повертає ім'я хоста, з яким встановлено задане з'єднання PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить ім'я підключеного через `connection` хоста, або порожній рядок у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгhost()****

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   print "Успешно подключились к : " . pg_host($pgsql_conn) . "<br/>\n";
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```

### Дивіться також

-   [пгconnect()](function.pg-connect.md) - Відкриває з'єднання з базою даних PostgreSQL
-   [пгpconnect()](function.pg-pconnect.md) - Відкриває постійне з'єднання із сервером PostgreSQL
