---
navigation:
  - mysqli.connect-error.md: '« mysqli::$connect\_error'
  - mysqli.debug.md: 'mysqli::debug »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::\_\_construct

# mysqli::connect

# mysqli\_connect

(PHP 5, PHP 7, PHP 8)

mysqli::\_\_construct -- mysqli::connect -- mysqli\_connect — Встановлює нове з'єднання з сервером MySQL

### Опис

Об'єктно-орієнтований стиль

public**mysqli::\_\_construct**  
?string`$hostname` **`null`**,  
?string`$username` **`null`**,  
?string`$password` **`null`**,  
?string`$database` **`null`**,  
?int`$port` **`null`**,  
?string`$socket` **`null`**  
) .

```methodsynopsis
public mysqli::connect(    ?string $hostname = null,    ?string $username = null,    ?string $password = null,    ?string $database = null,    ?int $port = null,    ?string $socket = null): bool
```

Процедурний стиль

```methodsynopsis
mysqli_connect(    ?string $hostname = null,    ?string $username = null,    ?string $password = null,    ?string $database = null,    ?int $port = null,    ?string $socket = null): mysqli|false
```

Встановлює з'єднання з працюючим сервером MySQL.

### Список параметрів

`hostname`

Може бути або ім'ям хоста, або IP-адресою. При передачі **`null`**, значение извлекается из[mysqli.default\_host](mysqli.configuration.md#ini.mysqli.default-host). По можливості замість протоколу TCP/IP використовуватимуться канали. Протокол TCP/IP використовується, якщо вказано ім'я хоста і номер порту, наприклад, `localhost:3308`

Якщо перед ім'ям хоста встановити рядок `p:`, то буде відкрито постійне з'єднання. Якщо з'єднання відкрито з пулу підключень, буде автоматично викликано функцію [mysqli\_change\_user()](mysqli.change-user.md)

`username`

Ім'я користувача MySQL або \*\*`null`\*\*для принятия имени пользователя на основе ini-опции[mysqli.default\_user](mysqli.configuration.md#ini.mysqli.default-user)

`password`

Пароль MySQL или\*\*`null`\*\*для принятия пароля на основе ini-опции[mysqli.default\_pw](mysqli.configuration.md#ini.mysqli.default-pw)

`database`

База даних за замовчуванням, яка буде використовуватися під час виконання запитів або **`null`**

`port`

Номер порту для спроби підключення до сервера MySQL або \*\*`null`\*\*для принятия порта на основе ini-опции[mysqli.default\_port](mysqli.configuration.md#ini.mysqli.default-port)

`socket`

Сокет або іменований пайп, який необхідно використовувати або \*\*`null`\*\*для принятия сокета на основе ini-опции[mysqli.default\_socket](mysqli.configuration.md#ini.mysqli.default-socket)

> **Зауваження** :
> 
> Передача параметра`socket` явно не буде задавати тип з'єднання при підключенні до сервера MySQL. Те, як встановлюватиметься з'єднання з MySQL-сервером, визначається параметром `hostname`

### Значення, що повертаються

[mysqli\_connect()](function.mysqli-connect.md) повертає об'єкт, який представляє з'єднання з сервером MySQL або \*\*`false`\*\*в случае возникновения ошибки.

[mysqli::connect()](function.mysqli-connect.md) повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. До PHP 8.1.0 у разі успішного виконання поверталося значення **`null`**

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Метод[mysqli::connect()](function.mysqli-connect.md) тепер повертає значення **`true`** замість **`null`** у разі успішного виконання. |
| 7.4.0 | Усі параметри тепер припускають значення **`null`** |

### Приклади

**Пример #1 Пример использования**mysqli::\_\_construct()\*\*\*\*

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

Висновок наведених прикладів буде схожим на:

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

> **Зауваження** :
> 
> MySQLnd завжди має на увазі кодування, яке використовує за умовчанням сервер. Це кодування передається під час встановлення з'єднання/авторизації, які використовує mysqlnd.
> 
> За замовчуванням Libmysqlclient використовує кодування, встановлене у файлі my.cnf або явним викликом функції [mysqli\_options()](mysqli.options.md) до виклику функції [mysqli\_real\_connect()](mysqli.real-connect.md), але після виклику функції [mysqli\_connect()](function.mysqli-connect.md)

> **Зауваження** :
> 
> Якщо використовується Об'єктно-орієнтований стиль: Якщо з'єднання встановити не вдалося, метод все одно поверне об'єкт. Перевірити успішність створення підключення можна або функцією [mysqli\_connect\_error()](mysqli.connect-error.md)или с помощью свойства[mysqli->connect\_error](mysqli.connect-error.md), Як показано в прикладах.

> **Зауваження** :
> 
> Якщо необхідно задати додаткові параметри підключення, на кшталт часу очікування і т.п., замість цього методу необхідно використовувати функцію [mysqli\_real\_connect()](mysqli.real-connect.md)

> **Зауваження** :
> 
> Виклик конструктора без параметрів ідентичний виклику функції [mysqli\_init()](mysqli.init.md)

> **Зауваження** :
> 
> Помилка "Can't create TCP/IP socket (10106)" зазвичай означає, що директива конфігурації [variables\_order](ini.core.md#ini.variables-order) не містить символ `E`. У Windows системах, якщо оточення не скопійовано, змінне середовище `SYSTEMROOT` буде недоступна, і у PHP виникнуть проблеми із завантаженням Winsock.

### Дивіться також

-   [mysqli\_real\_connect()](mysqli.real-connect.md) \- Встановлює з'єднання із сервером mysql
-   [mysqli\_options()](mysqli.options.md) \- Встановлення налаштувань
-   [mysqli\_connect\_errno()](mysqli.connect-errno.md) \- Повертає код помилки останньої спроби з'єднання
-   [mysqli\_connect\_error()](mysqli.connect-error.md) \- Повертає опис останньої помилки підключення
-   [mysqli\_close()](mysqli.close.md) \- Закриває раніше відкрите з'єднання з базою даних
