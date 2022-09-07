---
navigation:
  - mysqli.connect-error.md: '« mysqli::$connecterror'
  - mysqli.debug.md: 'mysqli::debug »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::construct'
---
# mysqli::construct

# mysqli::connect

# mysqliconnect

(PHP 5, PHP 7, PHP 8)

mysqli::construct -- mysqli::connect -- mysqliconnect — Встановлює нове з'єднання з сервером MySQL

### Опис

Об'єктно-орієнтований стиль

public **mysqli::construct**  
string `$hostname` = iniget("mysqli.defaulthost"),  
string `$username` = iniget("mysqli.defaultuser"),  
string `$password` = iniget("mysqli.defaultpw"),  
string `$database` = "",  
int `$port` = iniget("mysqli.defaultport"),  
string `$socket` = iniget("mysqli.defaultsocket")

```methodsynopsis
public mysqli::connect(    string $hostname = ini_get("mysqli.default_host"),    string $username = ini_get("mysqli.default_user"),    string $password = ini_get("mysqli.default_pw"),    string $database = "",    int $port = ini_get("mysqli.default_port"),    string $socket = ini_get("mysqli.default_socket")): void
```

Процедурний стиль

```methodsynopsis
mysqli_connect(    string $hostname = ini_get("mysqli.default_host"),    string $username = ini_get("mysqli.default_user"),    string $password = ini_get("mysqli.default_pw"),    string $database = "",    int $port = ini_get("mysqli.default_port"),    string $socket = ini_get("mysqli.default_socket")): mysqli|false
```

Встановлює з'єднання з працюючим сервером MySQL.

### Список параметрів

`hostname`

Може бути або ім'ям хоста, або IP-адресою. Передбачається використання локального хоста при вказанні у цьому параметрі **`null`** або рядка "localhost". По можливості замість протоколу TCP/IP використовуватимуться канали. Протокол TCP/IP використовується, якщо вказано ім'я хоста і номер порту, наприклад, `localhost:3308`

Якщо перед ім'ям хоста встановити рядок `p:`, то буде відкрито постійне з'єднання. Якщо з'єднання відкрито з пулу підключень, буде автоматично викликано функцію [mysqlichangeuser()](mysqli.change-user.md)

`username`

Ім'я користувача MySQL.

`password`

Якщо не заданий або дорівнює **`null`**, MySQL-сервер в першу чергу спробує аутентифікувати користувача в принципі, який має пароль, а потім буде шукати серед користувачів, у яких немає пароля. Такий підхід дозволяє одному користувачеві призначати різні права (залежно від того, задано пароль чи ні).

`database`

Якщо параметр встановлено, його значення буде використовуватися як ім'я бази даних за замовчуванням під час виконання запитів.

`port`

Вказує номер порту для підключення до сервера MySQL.

`socket`

Задає сокет або іменований пайп, який потрібно використовувати.

> **Зауваження**
> 
> Передача параметра `socket` явно не визначатиме тип з'єднання при підключенні до сервера MySQL. Те, як встановлюватиметься з'єднання з MySQL-сервером, визначається параметром `hostname`

### Значення, що повертаються

**mysqli::construct()** завжди повертає об'єкт, який представляє з'єднання з сервером MySQL, незалежно від того, було воно успішним чи ні.

[mysqliconnect()](function.mysqli-connect.md) повертає об'єкт, який представляє з'єднання з сервером MySQL або **`false`** у разі виникнення помилки.

[mysqli::connect()](function.mysqli-connect.md) повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Якщо **`MYSQLI_REPORT_STRICT`** увімкнена та під час підключення до бази даних сталася помилка, викидається [mysqlisqlexception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Приклад використання **mysqli::construct()****

Об'єктно-орієнтований стиль

```php
<?php

/* Вы должны включить отчёт об ошибках для mysqli, прежде чем пытаться установить соединение */
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);

$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'my_db');

/* Установите желаемую кодировку после установления соединения */
$mysqli->set_charset('utf8mb4');

printf("Успешно... %s\n", $mysqli->host_info);
?>
```

Процедурний стиль

```php
<?php

/* Вы должны включить отчёт об ошибках для mysqli, прежде чем пытаться установить соединение */
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);

$mysqli = mysqli_connect('localhost', 'my_user', 'my_password', 'my_db');

/* Установите желаемую кодировку после установления соединения */
mysqli_set_charset($mysqli, 'utf8mb4');

printf("Успешно... %s\n", mysqli_get_host_info($mysqli));
```

Результатом виконання даних прикладів буде щось подібне:

```
Успешно... localhost via TCP/IP
```

**Приклад #2 Розширення класу mysqli**

```php
<?php

class FooMysqli extends mysqli {
    public function __construct($host, $user, $pass, $db, $port, $socket, $charset) {
        mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
        parent::__construct($host, $user, $pass, $db, $port, $socket);
        $this->set_charset($charset);
    }
}

$db = new FooMysqli('localhost', 'my_user', 'my_password', 'my_db', 3306, null, 'utf8mb4');
```

**Приклад #3 Ручна обробка помилок**

Якщо звіти про помилки вимкнуто, розробник несе відповідальність за перевірку та обробку помилок

Об'єктно-орієнтований стиль

```php
<?php

error_reporting(0);
mysqli_report(MYSQLI_REPORT_OFF);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'my_db');
if ($mysqli->connect_errno) {
    throw new RuntimeException('ошибка соединения mysqli: ' . $mysqli->connect_error);
}

/* Установите желаемую кодировку после установления соединения */
$mysqli->set_charset('utf8mb4');
if ($mysqli->errno) {
    throw new RuntimeException('ошибка mysqli: ' . $mysqli->error);
}
```

Процедурний стиль

```php
<?php

error_reporting(0);
mysqli_report(MYSQLI_REPORT_OFF);
$mysqli = mysqli_connect('localhost', 'my_user', 'my_password', 'my_db');
if (mysqli_connect_errno()) {
    throw new RuntimeException('ошибка соединения mysqli: ' . mysqli_connect_error());
}

/* Установите желаемую кодировку после установления соединения */
mysqli_set_charset($mysqli, 'utf8mb4');
if (mysqli_errno($mysqli)) {
    throw new RuntimeException('ошибка mysqli: ' . mysqli_error($mysqli));
}
```

### Примітки

> **Зауваження**
> 
> MySQLnd завжди має на увазі кодування, яке використовує за умовчанням сервер. Це кодування передається під час встановлення з'єднання/авторизації, які використовує mysqlnd.
> 
> За замовчуванням Libmysqlclient використовує кодування, встановлене в my.cnf або спеціальним викликом [mysqlioptions()](mysqli.options.md) до використання [mysqlirealconnect()](mysqli.real-connect.md), але після [mysqliinit()](mysqli.init.md)

> **Зауваження**
> 
> Якщо використовується Об'єктно-орієнтований стиль: Якщо з'єднання встановити не вдалося, метод все одно поверне об'єкт. Перевірити успішність створення підключення можна або функцією [mysqliconnecterror()](mysqli.connect-error.md) або за допомогою властивості [mysqli->connecterror](mysqli.connect-error.md), Як показано в прикладах.

> **Зауваження**
> 
> Якщо необхідно задати додаткові параметри підключення, на кшталт часу очікування і т.п., замість цього методу необхідно використовувати функцію [mysqlirealconnect()](mysqli.real-connect.md)

> **Зауваження**
> 
> Виклик конструктора без параметрів ідентичний виклику функції [mysqliinit()](mysqli.init.md)

> **Зауваження**
> 
> Помилка "Can't create TCP/IP socket (10106)" зазвичай означає, що директива конфігурації [variablesorder](ini.core.md#ini.variables-order) не містить символ `E`. У Windows системах, якщо оточення не скопійовано, змінне середовище `SYSTEMROOT` буде недоступна, і у PHP виникнуть проблеми із завантаженням Winsock.

### Дивіться також

-   [mysqlirealconnect()](mysqli.real-connect.md) - Встановлює з'єднання із сервером mysql
-   [mysqlioptions()](mysqli.options.md) - Встановлення налаштувань
-   [mysqliconnecterrno()](mysqli.connect-errno.md) - Повертає код помилки останньої спроби з'єднання
-   [mysqliconnecterror()](mysqli.connect-error.md) - Повертає опис останньої помилки підключення
-   [mysqliclose()](mysqli.close.md) - Закриває раніше відкрите з'єднання з базою даних
