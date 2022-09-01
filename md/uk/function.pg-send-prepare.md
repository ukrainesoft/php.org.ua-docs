---
navigation:
  - function.pg-send-execute.html: « pgsendexecute
  - function.pg-send-query-params.html: пгsendqueryparams »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгsendprepare
---
# пгsendprepare

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгsendprepare — Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення

### Опис

```methodsynopsis
pg_send_prepare(PgSql\Connection $connection, string $statement_name, string $query): int|bool
```

Надсилає запит на створення параметризованого SQL виразу і не чекає на його завершення.

Це асинхронна версія функції [пгprepare()](function.pg-prepare.html): вона повертає **`true`**, якщо вдалося надіслати запит, **`false`** в іншому випадку. Після успішного надсилання, скористайтеся функцією [пгgetresult()](function.pg-get-result.html), щоб дізнатися, чи створився необхідний вираз SQL. Аргументи функції обробляються так само, як у [пгprepare()](function.pg-prepare.html). Функція не працюватиме з серверами PostgreSQL версій нижче 7.4.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

`statement_name`

Ім'я заготовки, що створюється. Має бути унікальним у межах сесії. Якщо встановлено порожній рядок, буде створено безіменний SQL вираз. При цьому він перезапише вже існуючий безіменний вираз, визначений раніше.

`query`

Параметризований запит SQL. Повинен містити лише один вираз (кілька виразів розділених крапкою з комою не підтримуються). Якщо в запит будуть передаватися параметри, вони замінять псевдозмінні $1, $2 і т.д.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, **`false`** або `0` у разі виникнення помилки. Для отримання результату запиту скористайтеся функцією [пгgetresult()](function.pg-get-result.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгsendprepare()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  // Подготовка запроса
  if (!pg_connection_busy($dbconn)) {
    pg_send_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');
    $res1 = pg_get_result($dbconn);
  }

  // Запуск запроса на выполнение. Стоит отметить, что нет необходимости экранировать
  // спецсимволы в строке "Joe's Widgets"
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Joe's Widgets"));
    $res2 = pg_get_result($dbconn);
  }

  // Запуск на выполнение того же запроса, но с другим параметром
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));
    $res3 = pg_get_result($dbconn);
  }

?>
```

### Дивіться також

-   [пгconnect()](function.pg-connect.html) - Відкриває з'єднання з базою даних PostgreSQL
-   [пгpconnect()](function.pg-pconnect.html) - Відкриває постійне з'єднання із сервером PostgreSQL
-   [пгexecute()](function.pg-execute.html) - Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
-   [пгsendexecute()](function.pg-send-execute.html) - Запускає попередньо підготовлений SQL-запит та передає йому параметри; не чекає результату, що повертається
-   [пгsendqueryparams()](function.pg-send-query-params.html) - Посилає параметризований запит на сервер, не чекає результату, що повертається.
