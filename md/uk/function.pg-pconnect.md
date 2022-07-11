- [« pg_parameter_status](function.pg-parameter-status.md)
- [pg_ping»](function.pg-ping.md)

- [PHP Manual](index.md)
- [Функції PostgreSQL](ref.pgsql.md)
- Відкриває постійне з'єднання із сервером PostgreSQL

#pg_pconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

pg_pconnect — Відкриває постійне з'єднання із сервером PostgreSQL

### Опис

**pg_pconnect**(string `$connection_string`, int `$flags` = 0):
[PgSql\Connection](class.pgsql-connection.md)\|false

**pg_pconnect()** встановлює з'єднання з базою даних PostgreSQL.
Повертає екземпляр [PgSql\Connection](class.pgsql-connection.md),
необхідний роботи більшості функцій PostgreSQL.

При повторному виклику функції **pg_pconnect()** з тими самими значеннями
параметрів в `connection_string` функція поверне існуюче
підключення. Щоб примусово створити нове з'єднання, необхідно
передати рядок підключення функції **`PGSQL_CONNECT_FORCE_NEW`**
як параметр `flags`.

Можливість створення постійних підключень регулюється директивою
[pgsql.allow_persistent](pgsql.configuration.md#ini.pgsql.allow-persistent)
файлу `php.ini`. Щоб увімкнути, встановіть значення в "On" (є
значенням за замовчуванням). Максимальна кількість постійних з'єднань
задається директивою
[pgsql.max_persistent](pgsql.configuration.md#ini.pgsql.max-persistent)
файлу `php.ini` (за замовчуванням -1, не обмежено). Кількість будь-яких
можливих підключень встановлюється директивою
[pgsql.max_links](pgsql.configuration.md#ini.pgsql.max-links) файлу
`php.ini`.

[pg_close()](function.pg-close.md) не закриває відкриті з'єднання
функцією **pg_pconnect()**.

### Список параметрів

`connection_string`
Рядок `connection_string` може бути порожнім рядком або містити
кілька параметрів розділених пробілами. Кожен параметр вказується
як `keyword=value`. Прогалини навколо знака і необов'язкові. Порожні
рядки як значення або значення, що містять пробіли відокремлюються
одинарними лапками, як, наприклад, `keyword = 'a value'`. Для завдання
одинарних лапок і зворотних слішів як значень їх необхідно
екранувати зворотним слішем, тобто \' і \\.

Список основних ключових слів: `host`, `hostaddr`, `port`, `dbname`
(значення за замовчуванням для параметра `user`), `user`, `password`,
`connect_timeout`, `options`, `tty` (ігнорується), `sslmode`,
`requiressl` (застаріло у зв'язку з використанням параметра `sslmode`), та
`Service`. Які з цих аргументів буде оброблено, залежить від версії
PostgreSQL.

`flags`
Якщо у функцію передано константу **`PGSQL_CONNECT_FORCE_NEW`**, буде
створювати нове підключення, навіть якщо `connection_string` ідентична
рядку існуючого підключення.

### Значення, що повертаються

Примірник [PgSql\Connection](class.pgsql-connection.md) у разі
успішного виконання або **`false`** у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                                 |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| 8.1.0  | Повертає екземпляр [PgSql\Connection](class.pgsql-connection.md); раніше повертався ресурс ([resource](language.types.resource.md)). |

### Приклади

**Приклад #1 Приклад використання **pg_pconnect()****

`<?php$dbconn = pg_pconnect("dbname=mary");//підключитися к базі "mary"$dbconn2 = pg_pconnect("host=localhost port=5432 dbname=mary");// підключитися на хості "localhost", порт "5432"$dbconn3 = pg_pconnect("host=sheep port=5432 dbname=mary user=lamb password=foo");//підключитися до хості| користувача і пароль$conn_string = "host=sheep port=5432 dbname=test user=lamb password=bar";$dbconn4 = pg_pconnect($conn_string);//підключитися к базі я і пароль?> `

### Дивіться також

- [pg_connect()](function.pg-connect.md) - Відкриває з'єднання з
базою даних PostgreSQL
- [Постійні з'єднання з базою даних](features.persistent-connections.md)
