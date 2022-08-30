Відкриває постійне з'єднання із сервером PostgreSQL

-   [« pgparameterstatus](function.pg-parameter-status.html)
    
-   [пгping »](function.pg-ping.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Відкриває постійне з'єднання із сервером PostgreSQL
    

# пгpconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

пгpconnect — Відкриває постійне з'єднання з сервером PostgreSQL

### Опис

```methodsynopsis
pg_pconnect(string $connection_string, int $flags = 0): PgSql\Connection|false
```

**пгpconnect()** встановлює з'єднання з базою даних PostgreSQL. Повертає екземпляр [PgSqlConnection](class.pgsql-connection.html), необхідний роботи більшості функцій PostgreSQL.

При повторному виклику функції **пгpconnect()** з тими ж значеннями параметрів `connection_string` функція поверне існуюче підключення. Щоб примусово створити нове з'єднання, необхідно надіслати рядок підключення функції **`PGSQL_CONNECT_FORCE_NEW`** як параметр `flags`

Можливість створення постійних підключень регулюється директивою [pgsql.allowpersistent](pgsql.configuration.html#ini.pgsql.allow-persistent) файлу php.ini. Щоб увімкнути, встановіть значення "On" (за замовчуванням). Максимальна кількість постійних з'єднань задається директивою [pgsql.maxpersistent](pgsql.configuration.html#ini.pgsql.max-persistent) файлу php.ini (за замовчуванням –1, не обмежено). Кількість будь-яких можливих підключень встановлюється директивою [pgsql.maxlinks](pgsql.configuration.html#ini.pgsql.max-links) файлу php.ini.

[пгclose()](function.pg-close.html) не закриває з'єднання, відкриті функцією **пгpconnect()**

### Список параметрів

`connection_string`

Рядок `connection_string` може бути порожнім рядком або містити кілька параметрів розділених пробілами. Кожен параметр вказується як `keyword = value`. Прогалини навколо знака однаково необов'язкові. Порожні рядки як значення або значення, що містять пробіли, відокремлюються одинарними лапками, як наприклад, `keyword = 'a value'`. Для завдання одинарних лапок і зворотних слішів як значення їх необхідно екранувати зворотним слешем, тобто ' і

Список основних ключових слів: `host` `hostaddr` `port` `dbname` (значення за замовчуванням для параметра `user` `user` `password` `connect_timeout` `options` `tty` (ігнорується), `sslmode` `requiressl` (застаріло у зв'язку з використанням параметра `sslmode`), і `service`. Які з цих аргументів будуть опрацьовані, залежить від версії PostgreSQL.

`flags`

Якщо у функцію передано константу **`PGSQL_CONNECT_FORCE_NEW`**, буде створюватися нове підключення, навіть якщо `connection_string` ідентична рядку існуючого підключення.

### Значення, що повертаються

Екземпляр [PgSqlConnection](class.pgsql-connection.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                            |
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
|        | Повертає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгpconnect()****

```php
<?php
$dbconn = pg_pconnect("dbname=mary");
//подключиться к базе "mary"

$dbconn2 = pg_pconnect("host=localhost port=5432 dbname=mary");
// подключиться к базе "mary" на хосте "localhost", порт "5432"

$dbconn3 = pg_pconnect("host=sheep port=5432 dbname=mary user=lamb password=foo");
//подключиться к базе "mary" на хосте "sheep", используя имя пользователя и пароль

$conn_string = "host=sheep port=5432 dbname=test user=lamb password=bar";
$dbconn4 = pg_pconnect($conn_string);
//подключиться к базе "test" на хосте "sheep", используя имя пользователя и пароль
?>
```

### Дивіться також

-   [пгconnect()](function.pg-connect.html) - Відкриває з'єднання з базою даних PostgreSQL
-   [Постійні з'єднання з базою даних](features.persistent-connections.html)