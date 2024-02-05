---
navigation:
  - mysqli.query.md: '« mysqli::query'
  - mysqli.real-escape-string.md: 'mysqli::real\_escape\_string »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::real\_connect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::real\_connect

# mysqli\_real\_connect

(PHP 5, PHP 7, PHP 8)

mysqli::real\_connect -- mysqli\_real\_connect — Встановлює з'єднання з сервером mysql

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::real_connect(    ?string $hostname = null,    ?string $username = null,    ?string $password = null,    ?string $database = null,    ?int $port = null,    ?string $socket = null,    int $flags = 0): bool
```

Процедурний стиль

```methodsynopsis
mysqli_real_connect(    mysqli $mysql,    ?string $hostname = null,    ?string $username = null,    ?string $password = null,    ?string $database = null,    ?int $port = null,    ?string $socket = null,    int $flags = 0): bool
```

Встановлює з'єднання із СУБД MySQL.

Ця функція відрізняється від [mysqli\_connect()](function.mysqli-connect.md) :

-   Для роботи\*\*mysqli\_real\_connect()\*\*необхідний дійсний об'єкт, створений функцією[mysqli\_init()](mysqli.init.md)
    
-   За допомогою функції[mysqli\_options()](mysqli.options.md)можна встановити різні настройки підключення.
    
-   Параметр`flags`
    

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`hostname`

Може бути або ім'ям хоста, або IP-адресою. При передачі **`null`**, значение извлекается из[mysqli.default\_host](mysqli.configuration.md#ini.mysqli.default-host). По можливості замість протоколу TCP/IP використовуватимуться канали. Протокол TCP/IP використовується, якщо вказано ім'я хоста і номер порту, наприклад, `localhost:3308`

`username`

Ім'я користувача MySQL або \*\*`null`\*\*для принятия имени пользователя на основе ini-опции[mysqli.default\_user](mysqli.configuration.md#ini.mysqli.default-user)

`password`

Пароль MySQL или\*\*`null`\*\*для принятия пароля на основе ini-опции[mysqli.default\_pw](mysqli.configuration.md#ini.mysqli.default-pw)

`database`

База даних за замовчуванням, яка буде використовуватися під час виконання запитів або **`null`**

`port`

Номер порту для спроби підключення до сервера MySQL або \*\*`null`\*\*для принятия порта на основе ini-опции[mysqli.default\_port](mysqli.configuration.md#ini.mysqli.default-port)

`socket`

Вказує номер порту для підключення до сервера MySQL.

> **Зауваження** :
> 
> Передача параметра`socket` явно не буде задавати тип з'єднання при підключенні до сервера MySQL. Те, як встановлюватиметься з'єднання з MySQL-сервером, визначається параметром `hostname`

`flags`

С помощью параметра`flags` можна встановити деякі налаштування з'єднання:

**Прапори, що підтримуються**

| Имя | Опис |
| --- | --- |
| **`MYSQLI_CLIENT_COMPRESS`** | Використовувати протокол стиснення |
| **`MYSQLI_CLIENT_FOUND_ROWS`** | Повертати кількість рядків, що підійшли умовам вибірки, замість кількості порушених запитом рядків |
| **`MYSQLI_CLIENT_IGNORE_SPACE`** | Допускати пробіли після назв функцій. Робить усі імена функцій зарезервованими словами. |
| **`MYSQLI_CLIENT_INTERACTIVE`** | Допускати `interactive_timeout`секунд (вместо`wait_timeout`) простою, перш ніж закрити з'єднання |
| **`MYSQLI_CLIENT_SSL`** | Використовувати SSL (шифрування) |
| **`MYSQLI_CLIENT_SSL_DONT_VERIFY_SERVER_CERT`** | Аналогічно **`MYSQLI_CLIENT_SSL`**, але забороняє перевірку сертифіката SSL. Працює тільки з MySQL Native Driver та MySQL 5.6 та вище. |

> **Зауваження** :
> 
> З причин безпеки, прапор **`MULTI_STATEMENT`** не підтримується у PHP. Якщо потрібно виконувати мультизапити, використовуйте функцію [mysqli\_multi\_query()](mysqli.multi-query.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Усі параметри тепер припускають значення **`null`** |

### Приклади

**Приклад #1 Приклад використання** mysqli::real\_connect()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

$mysqli = mysqli_init();
if (!$mysqli) {
    die('mysqli_init завершилась провалом');
}

if (!$mysqli->options(MYSQLI_INIT_COMMAND, 'SET AUTOCOMMIT = 0')) {
    die('Установка MYSQLI_INIT_COMMAND завершилась провалом');
}

if (!$mysqli->options(MYSQLI_OPT_CONNECT_TIMEOUT, 5)) {
    die('Установка MYSQLI_OPT_CONNECT_TIMEOUT завершилась провалом');
}

if (!$mysqli->real_connect('localhost', 'my_user', 'my_password', 'my_db')) {
    die('Ошибка подключения (' . mysqli_connect_errno() . ') '
            . mysqli_connect_error());
}

echo 'Выполнено... ' . $mysqli->host_info . "\n";

$mysqli->close();
?>
```

Об'єктно-орієнтований стиль при розширенні класу mysqli

```php
<?php

class foo_mysqli extends mysqli {
    public function __construct($host, $user, $pass, $db) {
        parent::__construct();

        if (!parent::options(MYSQLI_INIT_COMMAND, 'SET AUTOCOMMIT = 0')) {
            die('Установка MYSQLI_INIT_COMMAND завершилась провалом');
        }

        if (!parent::options(MYSQLI_OPT_CONNECT_TIMEOUT, 5)) {
            die('Установка MYSQLI_OPT_CONNECT_TIMEOUT завершилась провалом');
        }

        if (!parent::real_connect($host, $user, $pass, $db)) {
            die('Ошибка подключения (' . mysqli_connect_errno() . ') '
                    . mysqli_connect_error());
        }
    }
}

$db = new foo_mysqli('localhost', 'my_user', 'my_password', 'my_db');

echo 'Выполнено... ' . $db->host_info . "\n";

$db->close();
?>
```

Процедурний стиль

```php
<?php

$link = mysqli_init();
if (!$link) {
    die('mysqli_init завершилась провалом');
}

if (!mysqli_options($link, MYSQLI_INIT_COMMAND, 'SET AUTOCOMMIT = 0')) {
    die('Установка MYSQLI_INIT_COMMAND завершилась провалом');
}

if (!mysqli_options($link, MYSQLI_OPT_CONNECT_TIMEOUT, 5)) {
    die('Установка MYSQLI_OPT_CONNECT_TIMEOUT завершилась провалом');
}

if (!mysqli_real_connect($link, 'localhost', 'my_user', 'my_password', 'my_db')) {
    die('Ошибка подключения (' . mysqli_connect_errno() . ') '
            . mysqli_connect_error());
}

echo 'Выполнено... ' . mysqli_get_host_info($link) . "\n";

mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Выполнено... MySQL host info: localhost via TCP/IP
```

### Примітки

> **Зауваження** :
> 
> MySQLnd завжди має на увазі кодування, яке використовує за умовчанням сервер. Це кодування передається під час встановлення з'єднання/авторизації, які використовує mysqlnd.
> 
> За замовчуванням Libmysqlclient використовує кодування, встановлене у файлі my.cnf або явним викликом функції [mysqli\_options()](mysqli.options.md) до виклику функції **mysqli\_real\_connect()**, але після виклику функції [mysqli\_connect()](function.mysqli-connect.md)

### Дивіться також

-   [mysqli\_connect()](function.mysqli-connect.md) \- Псевдонім mysqli::\_\_construct
-   [mysqli\_init()](mysqli.init.md) \- Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqli\_real\_connect()
-   [mysqli\_options()](mysqli.options.md) \- Встановлення налаштувань
-   [mysqli\_ssl\_set()](mysqli.ssl-set.md) \- Використовується для встановлення безпечних з'єднань за допомогою SSL
-   [mysqli\_close()](mysqli.close.md) \- Закриває раніше відкрите з'єднання з базою даних
