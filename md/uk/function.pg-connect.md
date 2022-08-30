Відкриває з'єднання з базою даних PostgreSQL

-   [« pgconnectpoll](function.pg-connect-poll.html)
    
-   [пгconnectionbusy »](function.pg-connection-busy.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Відкриває з'єднання з базою даних PostgreSQL
    

# пгconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

пгconnect — Відкриває з'єднання з базою даних PostgreSQL

### Опис

```methodsynopsis
pg_connect(string $connection_string, int $flags = 0): PgSql\Connection|false
```

**пгconnect()** відкриває з'єднання з базою даних PostgreSQL, визначене рядком `connection_string`

При повторному виклику функції **пгconnect()** з тими ж значеннями параметрів `connection_string` функція поверне існуюче підключення. Щоб примусово створити нове з'єднання, необхідно надіслати рядок підключення функції **`PGSQL_CONNECT_FORCE_NEW`** як параметр `flags`

Колишній синтаксис із безліччю параметрів **$conn = pgconnect("host", "port", "options", "tty", "dbname")** вважається застарілим.

### Список параметрів

`connection_string`

Рядок `connection_string` може бути порожнім рядком або містити кілька параметрів, розділених пробілами. Кожен параметр вказується як `keyword = value`. Прогалини навколо знака "однаково" необов'язкові. Порожні рядки як значення або значення, що містять пробіли, відокремлюються одинарними лапками, як наприклад, `keyword = 'a value'`. Для запису одинарних лапок і зворотних слішів як значення, їх необхідно екранувати зворотним слешем, тобто ' і

Список основних ключових слів: `host` `hostaddr` `port` `dbname` (значення за замовчуванням для параметра `user` `user` `password` `connect_timeout` `options` `tty` (ігнорується), `sslmode` `requiressl` (застаріло у зв'язку з використанням параметра `sslmode`), та `service`. Які з цих аргументів будуть опрацьовані, залежить від версії PostgreSQL.

Параметр `options` служить для встановлення параметрів командного рядка, оброблених сервером.

`flags`

Якщо у функцію передано константу **`PGSQL_CONNECT_FORCE_NEW`**, буде створюватися нове підключення, навіть якщо `connection_string` ідентична рядку існуючого підключення.

Якщо передана константа **`PGSQL_CONNECT_ASYNC`**, то з'єднання встановлюється асинхронним. Стан з'єднання можна перевірити за допомогою функцій [пгconnectpoll()](function.pg-connect-poll.html) або [пгconnectionstatus()](function.pg-connection-status.html)

### Значення, що повертаються

Повертає екземпляр [PgSqlConnection](class.pgsql-connection.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                              |
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
|        | Повертає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше повертався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Використання функції **пгconnect()****

```php
<?php
$dbconn = pg_connect("dbname=mary");
//подключиться к базе "mary"

$dbconn2 = pg_connect("host=localhost port=5432 dbname=mary");
//подключиться к базе "mary" на хосте "localhost", порт "5432"

$dbconn3 = pg_connect("host=sheep port=5432 dbname=mary user=lamb password=foo");
//подключиться к базе "mary" на хосте "sheep", используя имя пользователя и пароль

$conn_string = "host=sheep port=5432 dbname=test user=lamb password=bar";
$dbconn4 = pg_connect($conn_string);
//подключиться к базе "test" на хосте "sheep", используя имя пользователя и пароль

$dbconn5 = pg_connect("host=localhost options='--client_encoding=UTF8'");
//подключиться к базе на хосте "localhost" и передать параметр командной строки, задающий кодировку UTF-8
?>
```

### Дивіться також

-   [пгpconnect()](function.pg-pconnect.html) - Відкриває постійне з'єднання із сервером PostgreSQL
-   [пгclose()](function.pg-close.html) - Закриває з'єднання з базою даних PostgreSQL
-   [пгhost()](function.pg-host.html) - Повертає ім'я хоста, що відповідає підключенню
-   [пгport()](function.pg-port.html) - Повертає номер порту, який відповідає заданому з'єднанню
-   [пгtty()](function.pg-tty.html) - Повертає ім'я терміналу TTY, пов'язане зі з'єднанням
-   [пгoptions()](function.pg-options.html) - Отримання параметрів з'єднання із сервером баз даних
-   [пгdbname()](function.pg-dbname.html) - Визначає ім'я бази даних