---
navigation:
  - function.pg-send-execute.md: « pg\_send\_execute
  - function.pg-send-query-params.md: pg\_send\_query\_params »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_send\_prepare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_send\_prepare

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_send\_prepare — Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення

### Опис

```methodsynopsis
pg_send_prepare(PgSql\Connection $connection, string $statement_name, string $query): int|bool
```

Надсилає запит на створення параметризованого SQL виразу і не чекає на його завершення.

Це асинхронна версія функції [pg\_prepare()](function.pg-prepare.md): вона повертає **`true`**, якщо вдалося надіслати запит, **`false`** в іншому випадку. Після успішного надсилання, скористайтеся функцією [pg\_get\_result()](function.pg-get-result.md), щоб дізнатися, чи створився необхідний вираз SQL. Аргументи функції обробляються так само, як у [pg\_prepare()](function.pg-prepare.md). Функція не працюватиме з серверами PostgreSQL версій нижче 7.4.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`statement_name`

Ім'я заготовки, що створюється. Має бути унікальним у межах сесії. Якщо встановлено порожній рядок, буде створено безіменний SQL вираз. При цьому він перезапише вже існуючий безіменний вираз, визначений раніше.

`query`

Параметризований запит SQL. Повинен містити лише один вираз (кілька виразів розділених крапкою з комою не підтримуються). Якщо в запит будуть передаватися параметри, вони замінять псевдозмінні $1, $2 і т.д.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, \*\*`false`\*\*или в случае возникновения ошибки. Для получения результата запроса используйте функцию[pg\_get\_result()](function.pg-get-result.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_send\_prepare()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  // Подготовка запроса
  if (!pg_connection_busy($dbconn)) {
    pg_send_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');
    $res1 = pg_get_result($dbconn);
  }

  // Запуск запроса на выполнение. Стоит отметить, что нет необходимости экранировать
  // спецсимволы в строке "Joe's Widgets"
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Joe's Widgets"));
    $res2 = pg_get_result($dbconn);
  }

  // Запуск на выполнение того же запроса, но с другим параметром
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));
    $res3 = pg_get_result($dbconn);
  }

?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.md) \- Відкриває з'єднання з базою даних PostgreSQL
-   [pg\_pconnect()](function.pg-pconnect.md) \- Відкриває постійне з'єднання із сервером PostgreSQL
-   [pg\_execute()](function.pg-execute.md) \- Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
-   [pg\_send\_execute()](function.pg-send-execute.md) \- Запускає попередньо підготовлений SQL-запит та передає йому параметри; не чекає результату, що повертається
-   [pg\_send\_query\_params()](function.pg-send-query-params.md) \- Посилає параметризований запит на сервер, не чекає результату, що повертається.
