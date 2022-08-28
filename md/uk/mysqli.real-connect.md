Встановлює з'єднання з сервером mysql

-   [« mysqli::query](mysqli.query.html)
    
-   [mysqli::real\_escape\_string »](mysqli.real-escape-string.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Встановлює з'єднання з сервером mysql
    

# mysqli::realconnect

# mysqlirealconnect

(PHP 5, PHP 7, PHP 8)

mysqli::realconnect -- mysqlirealconnect — Встановлює з'єднання з сервером mysql

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::real_connect(    string $host = ?,    string $username = ?,    string $passwd = ?,    string $dbname = ?,    int $port = ?,    string $socket = ?,    int $flags = ?): bool
```

Процедурний стиль

```methodsynopsis
mysqli_real_connect(    mysqli $link,    string $host = ?,    string $username = ?,    string $passwd = ?,    string $dbname = ?,    int $port = ?,    string $socket = ?,    int $flags = ?): bool
```

Встановлює з'єднання із СУБД MySQL.

Ця функція відрізняється від [mysqli\_connect()](function.mysqli-connect.html)

-   Для роботи **mysqlirealconnect()** необхідний дійсний об'єкт, створений функцією [mysqli\_init()](mysqli.init.html)
    
-   За допомогою функції [mysqli\_options()](mysqli.options.html) можна встановити різні налаштування підключення.
    
-   Параметр `flags`
    

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`host`

Може бути ім'ям хоста або IP-адресою. Передача **`null`** або рядка "localhost" цього параметра означає, що як хост буде використовуватися локальна машина, на якій запущено скрипт. Якщо така можливість, будуть використовуватися пайпи замість протоколу TCP/IP.

`username`

Ім'я користувача MySQL.

`passwd`

Якщо не заданий або дорівнює **`null`**, MySQL-сервер в першу чергу спробує аутентифікувати користувача в принципі, який має пароль, а потім буде шукати серед користувачів, у яких немає пароля. Такий підхід дозволяє одному користувачеві призначати різні права (залежно від того, задано пароль чи ні).

`dbname`

Якщо параметр встановлено, його значення буде використовуватися як ім'я бази даних за замовчуванням під час виконання запитів.

`port`

Порт, до якого буде здійснюватись підключення.

`socket`

Вказує номер порту для підключення до сервера MySQL.

> **Зауваження**
> 
> Передача параметра `socket` явно не визначатиме тип з'єднання при підключенні до сервера MySQL. Те, як встановлюватиметься з'єднання з MySQL-сервером, визначається параметром `host`

`flags`

За допомогою параметра `flags` можна встановити деякі налаштування з'єднання:

**Прапори, що підтримуються**

| Имя                                             | Описание                                                                                                                               |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **`MYSQLI_CLIENT_COMPRESS`**                    | Використовувати протокол стиснення                                                                                                     |
| **`MYSQLI_CLIENT_FOUND_ROWS`**                  | Повертати кількість рядків, що підійшли умовам вибірки, замість кількості порушених запитом рядків                                     |
| **`MYSQLI_CLIENT_IGNORE_SPACE`**                | Допускати пробіли після назв функцій. Робить усі імена функцій зарезервованими словами.                                                |
| **`MYSQLI_CLIENT_INTERACTIVE`**                 | Допускати `interactive_timeout` секунд (замість `wait_timeout`) простою, перш ніж закрити з'єднання                                    |
| **`MYSQLI_CLIENT_SSL`**                         | Використовувати SSL (шифрування)                                                                                                       |
| **`MYSQLI_CLIENT_SSL_DONT_VERIFY_SERVER_CERT`** | Аналогічно **`MYSQLI_CLIENT_SSL`**, але забороняє перевірку сертифіката SSL. Працює тільки з MySQL Native Driver та MySQL 5.6 та вище. |

> **Зауваження**
> 
> З причин безпеки, прапор **`MULTI_STATEMENT`** не підтримується у PHP. Якщо потрібно виконувати мультизапити, використовуйте функцію [mysqli\_multi\_query()](mysqli.multi-query.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::realconnect()****

Об'єктно-орієнтований стиль

```php
<?php

$mysqli = mysqli_init();
if (!$mysqli) {
    die('mysqli_init завершилась провалом');
}

if (!$mysqli->options(MYSQLI_INIT_COMMAND, 'SET AUTOCOMMIT = 0')) {
    die('Установка MYSQLI_INIT_COMMAND завершилась провалом');
}

if (!$mysqli->options(MYSQLI_OPT_CONNECT_TIMEOUT, 5)) {
    die('Установка MYSQLI_OPT_CONNECT_TIMEOUT завершилась провалом');
}

if (!$mysqli->real_connect('localhost', 'my_user', 'my_password', 'my_db')) {
    die('Ошибка подключения (' . mysqli_connect_errno() . ') '
            . mysqli_connect_error());
}

echo 'Выполнено... ' . $mysqli->host_info . "\n";

$mysqli->close();
?>
```

Об'єктно-орієнтований стиль при розширенні класу mysqli

```php
<?php

class foo_mysqli extends mysqli {
    public function __construct($host, $user, $pass, $db) {
        parent::init();

        if (!parent::options(MYSQLI_INIT_COMMAND, 'SET AUTOCOMMIT = 0')) {
            die('Установка MYSQLI_INIT_COMMAND завершилась провалом');
        }

        if (!parent::options(MYSQLI_OPT_CONNECT_TIMEOUT, 5)) {
            die('Установка MYSQLI_OPT_CONNECT_TIMEOUT завершилась провалом');
        }

        if (!parent::real_connect($host, $user, $pass, $db)) {
            die('Ошибка подключения (' . mysqli_connect_errno() . ') '
                    . mysqli_connect_error());
        }
    }
}

$db = new foo_mysqli('localhost', 'my_user', 'my_password', 'my_db');

echo 'Выполнено... ' . $db->host_info . "\n";

$db->close();
?>
```

Процедурний стиль

```php
<?php

$link = mysqli_init();
if (!$link) {
    die('mysqli_init завершилась провалом');
}

if (!mysqli_options($link, MYSQLI_INIT_COMMAND, 'SET AUTOCOMMIT = 0')) {
    die('Установка MYSQLI_INIT_COMMAND завершилась провалом');
}

if (!mysqli_options($link, MYSQLI_OPT_CONNECT_TIMEOUT, 5)) {
    die('Установка MYSQLI_OPT_CONNECT_TIMEOUT завершилась провалом');
}

if (!mysqli_real_connect($link, 'localhost', 'my_user', 'my_password', 'my_db')) {
    die('Ошибка подключения (' . mysqli_connect_errno() . ') '
            . mysqli_connect_error());
}

echo 'Выполнено... ' . mysqli_get_host_info($link) . "\n";

mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Выполнено... MySQL host info: localhost via TCP/IP
```

### Примітки

> **Зауваження**
> 
> MySQLnd завжди має на увазі кодування, яке використовує за умовчанням сервер. Це кодування передається під час встановлення з'єднання/авторизації, які використовує mysqlnd.
> 
> Libmysqlclient за умовчанням використовує кодування, встановлене в my.cnf або спеціальним викликом [mysqli\_options()](mysqli.options.html) до використання **mysqlirealconnect()**, але після [mysqli\_init()](mysqli.init.html)

### Дивіться також

-   [mysqli\_connect()](function.mysqli-connect.html) - Псевдонім mysqli::construct
-   [mysqli\_init()](mysqli.init.html) - Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()
-   [mysqli\_options()](mysqli.options.html) - Встановлення налаштувань
-   [mysqli\_ssl\_set()](mysqli.ssl-set.html) - Використовується для встановлення безпечних з'єднань за допомогою SSL
-   [mysqli\_close()](mysqli.close.html) - Закриває раніше відкрите з'єднання з базою даних