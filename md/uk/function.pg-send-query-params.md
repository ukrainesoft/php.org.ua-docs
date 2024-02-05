---
navigation:
  - function.pg-send-prepare.md: « pg\_send\_prepare
  - function.pg-send-query.md: pg\_send\_query »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_send\_query\_params
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_send\_query\_params

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_send\_query\_params — Посилає параметризований запит на сервер, не чекає результату, що повертається.

### Опис

```methodsynopsis
pg_send_query_params(PgSql\Connection $connection, string $query, array $params): int|bool
```

Надсилає параметризований запит на виконання і не чекає на його завершення. Параметри передаються окремо від тексту запиту SQL.

Функція є аналогом [pg\_send\_query()](function.pg-send-query.md) за одним винятком: параметри запиту можна надсилати окремо від рядка запиту. Аргументи функції обробляються так само, як і в [pg\_query\_params()](function.pg-query-params.md). . [pg\_send\_query()](function.pg-send-query.md) підтримується на з'єднаннях із серверами PostgreSQL версій 7.4 та вище. Функція не працюватиме із серверами ранніх версій. Також вона підтримує лише одну SQL-команду у виразі.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`query`

Параметризований запит SQL. Повинен містити лише один вираз (кілька виразів розділених крапкою з комою не підтримуються). Якщо в запит будуть передаватися параметри, вони замінять псевдозмінні $1, $2 і т.д.

`params`

Масив значень параметрів запиту для заміни псевдозмінних $1, $2 і т.д. у вихідному рядку запиту. Кількість елементів масиву має точно збігатися з кількістю псевдозмінних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, \*\*`false`\*\*или в случае возникновения ошибки. Для получения результата запроса используйте функцию[pg\_get\_result()](function.pg-get-result.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_send\_query\_params()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось подключиться");

  // Использование параметров. Стоит заметить, что нет необходимости
  // заключать в кавычки и экранировать параметр.
  pg_send_query_params($dbconn, 'select count(*) from authors where city = $1', array('Perth'));

  // В сравнении с pg_send_query
  $str = pg_escape_string('Perth');
  pg_send_query($dbconn, "select count(*) from authors where city = '${str}'");
?>
```

### Дивіться також

-   [pg\_send\_query()](function.pg-send-query.md) \- Надсилає асинхронний запит
