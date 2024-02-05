---
navigation:
  - function.pg-connect-poll.md: « pg\_connect\_poll
  - function.pg-connection-busy.md: pg\_connection\_busy »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_connect

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_connect — Відкриває з'єднання з базою даних PostgreSQL

### Опис

```methodsynopsis
pg_connect(string $connection_string, int $flags = 0): PgSql\Connection|false
```

**pg\_connect()** відкриває з'єднання з базою даних PostgreSQL, визначене рядком `connection_string`

При повторному виклику функції **pg\_connect()** з тими ж значеннями параметрів `connection_string` функція поверне існуюче підключення. Щоб примусово створити нове з'єднання, необхідно надіслати рядок підключення функції **`PGSQL_CONNECT_FORCE_NEW`** як параметр `flags`

Прежний синтаксис с множеством параметров\*\*$conn = pg\_connect("host", "port", "options", "tty", "dbname")\*\*считается устаревшим.

### Список параметрів

`connection_string`

Рядок `connection_string` може бути порожнім рядком або містити кілька параметрів, розділених пробілами. Кожен параметр вказується як `keyword = value`. . Прогалини навколо знака "однаково" необов'язкові. Порожні рядки як значення або значення, що містять пробіли, відокремлюються одинарними лапками, як наприклад, `keyword = 'a value'`. Для запису одинарних лапок і зворотних слішів як значення, їх необхідно екранувати зворотним слешем, тобто \\' і \\\\

Список основних ключових слів: `host` `hostaddr` `port` `dbname`(значение по умолчанию для параметра`user` `user` `password` `connect_timeout` `options` `tty` (ігнорується), `sslmode` `requiressl`(устарело в связи с использованием параметра`sslmode`), и`service`. Які з цих аргументів будуть опрацьовані, залежить від версії PostgreSQL.

Параметр`options` служить для встановлення параметрів командного рядка, оброблених сервером.

`flags`

Если в функцию передана константа\*\*`PGSQL_CONNECT_FORCE_NEW`\*\*, буде створюватися нове підключення, навіть якщо `connection_string` ідентична рядку існуючого підключення.

Если передана константа\*\*`PGSQL_CONNECT_ASYNC`\*\*, то з'єднання встановлюється асинхронним. Стан з'єднання можна перевірити за допомогою функцій [pg\_connect\_poll()](function.pg-connect-poll.md) або [pg\_connection\_status()](function.pg-connection-status.md)

### Значення, що повертаються

Повертає екземпляр [PgSql\\Connection](class.pgsql-connection.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Использование функции**pg\_connect()\*\*\*\*

```php
<?php
$dbconn = pg_connect("dbname=mary");
//подключиться к базе "mary"

$dbconn2 = pg_connect("host=localhost port=5432 dbname=mary");
//подключиться к базе "mary" на хосте "localhost", порт "5432"

$dbconn3 = pg_connect("host=sheep port=5432 dbname=mary user=lamb password=foo");
//подключиться к базе "mary" на хосте "sheep", используя имя пользователя и пароль

$conn_string = "host=sheep port=5432 dbname=test user=lamb password=bar";
$dbconn4 = pg_connect($conn_string);
//подключиться к базе "test" на хосте "sheep", используя имя пользователя и пароль

$dbconn5 = pg_connect("host=localhost options='--client_encoding=UTF8'");
//подключиться к базе на хосте "localhost" и передать параметр командной строки, задающий кодировку UTF-8
?>
```

### Дивіться також

-   [pg\_pconnect()](function.pg-pconnect.md) \- Відкриває постійне з'єднання із сервером PostgreSQL
-   [pg\_close()](function.pg-close.md) \- Закриває з'єднання з базою даних PostgreSQL
-   [pg\_host()](function.pg-host.md) \- Повертає ім'я хоста, що відповідає підключенню
-   [pg\_port()](function.pg-port.md) \- Повертає номер порту, який відповідає заданому з'єднанню
-   [pg\_tty()](function.pg-tty.md) \- Повертає ім'я терміналу TTY, пов'язане зі з'єднанням
-   [pg\_options()](function.pg-options.md) \- Отримання параметрів з'єднання із сервером баз даних
-   [pg\_dbname()](function.pg-dbname.md) \- Визначає ім'я бази даних
