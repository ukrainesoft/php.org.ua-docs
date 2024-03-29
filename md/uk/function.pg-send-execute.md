---
navigation:
  - function.pg-select.md: « pg\_select
  - function.pg-send-prepare.md: pg\_send\_prepare »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_send\_execute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_send\_execute

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_send\_execute - Запускає попередньо підготовлений SQL-запит і передає йому параметри; не чекає результату, що повертається

### Опис

```methodsynopsis
pg_send_execute(PgSql\Connection $connection, string $statement_name, array $params): int|bool
```

Запускає попередньо підготовлений SQL-запит та передає йому параметри; не чекає результату, що повертається.

Працює аналогічно до функцій [pg\_send\_query\_params()](function.pg-send-query-params.md), тільки замість рядка із запитом приймає ім'я попередньо підготовленого SQL-запиту. Аргументи функції обробляються так само, як і функції [pg\_execute()](function.pg-execute.md). Як і [pg\_execute()](function.pg-execute.md) ця функція не працюватиме на з'єднаннях з серверами PostgreSQL версій нижче 7.4.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`statement_name`

Ім'я підготовленого до виконання запиту. Якщо передано порожній рядок "", буде виконано безіменний запит. Ім'я та вміст запиту мають бути підготовлені функцією [pg\_prepare()](function.pg-prepare.md) [pg\_send\_prepare()](function.pg-send-prepare.md) або за допомогою SQL-команди `PREPARE`

`params`

Масив значень параметрів запиту для заміни псевдозмінних $1, $2 і т.д. у вихідному рядку запиту. Кількість елементів масиву має точно збігатися з кількістю псевдозмінних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, \*\*`false`\*\*или в случае возникновения ошибки. Для получения результата запроса используйте функцию[pg\_get\_result()](function.pg-get-result.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_send\_execute()\*\*\*\*

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

-   [pg\_prepare()](function.pg-prepare.md) \- Надсилає запит на створення параметризованого SQL виразу і чекає на його завершення
-   [pg\_send\_prepare()](function.pg-send-prepare.md) \- Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення
-   [pg\_execute()](function.pg-execute.md) \- Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
