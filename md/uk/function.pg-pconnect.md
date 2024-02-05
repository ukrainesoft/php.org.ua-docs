---
navigation:
  - function.pg-parameter-status.md: « pg\_parameter\_status
  - function.pg-ping.md: pg\_ping »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_pconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_pconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_pconnect — Відкриває постійне з'єднання з сервером PostgreSQL

### Опис

```methodsynopsis
pg_pconnect(string $connection_string, int $flags = 0): PgSql\Connection|false
```

**pg\_pconnect()** встановлює з'єднання з базою даних PostgreSQL. Повертає екземпляр [PgSql\\Connection](class.pgsql-connection.md), необхідний роботи більшості функцій PostgreSQL.

При повторному виклику функції **pg\_pconnect()** з тими ж значеннями параметрів `connection_string` функція поверне існуюче підключення. Щоб примусово створити нове з'єднання, необхідно надіслати рядок підключення функції **`PGSQL_CONNECT_FORCE_NEW`** як параметр `flags`

Можливість створення постійних підключень регулюється директивою [pgsql.allow\_persistent](pgsql.configuration.md#ini.pgsql.allow-persistent) файл php.ini. Щоб увімкнути, встановіть значення "On" (за замовчуванням). Максимальна кількість постійних з'єднань задається директивою [pgsql.max\_persistent](pgsql.configuration.md#ini.pgsql.max-persistent) файлу php.ini (за замовчуванням –1, не обмежено). Кількість будь-яких можливих підключень встановлюється директивою [pgsql.max\_links](pgsql.configuration.md#ini.pgsql.max-links)файла php.ini.

[pg\_close()](function.pg-close.md) не закриває з'єднання, відкриті функцією **pg\_pconnect()**

### Список параметрів

`connection_string`

Рядок `connection_string` може бути порожнім рядком або містити кілька параметрів розділених пробілами. Кожен параметр вказується як `keyword = value`. Прогалини навколо знака однаково необов'язкові. Порожні рядки як значення або значення, що містять пробіли, відокремлюються одинарними лапками, як наприклад, `keyword = 'a value'`. Для завдання одинарних лапок і зворотних слішів як значення їх необхідно екранувати зворотним слешем, тобто \\' і \\\\

Список основних ключових слів: `host` `hostaddr` `port` `dbname`(значение по умолчанию для параметра`user` `user` `password` `connect_timeout` `options` `tty` (ігнорується), `sslmode` `requiressl`(устарело в связи с использованием параметра`sslmode`), и`service`. Які з цих аргументів будуть опрацьовані, залежить від версії PostgreSQL.

`flags`

Если в функцию передана константа\*\*`PGSQL_CONNECT_FORCE_NEW`\*\*, буде створюватися нове підключення, навіть якщо `connection_string` ідентична рядку існуючого підключення.

### Значення, що повертаються

Екземпляр [PgSql\\Connection](class.pgsql-connection.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_pconnect()\*\*\*\*

```php
<?php
$dbconn = pg_pconnect("dbname=mary");
//подключиться к базе "mary"

$dbconn2 = pg_pconnect("host=localhost port=5432 dbname=mary");
// подключиться к базе "mary" на хосте "localhost", порт "5432"

$dbconn3 = pg_pconnect("host=sheep port=5432 dbname=mary user=lamb password=foo");
//подключиться к базе "mary" на хосте "sheep", используя имя пользователя и пароль

$conn_string = "host=sheep port=5432 dbname=test user=lamb password=bar";
$dbconn4 = pg_pconnect($conn_string);
//подключиться к базе "test" на хосте "sheep", используя имя пользователя и пароль
?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.md) \- Відкриває з'єднання з базою даних PostgreSQL
-   [Постійні з'єднання з базою даних](features.persistent-connections.md)
