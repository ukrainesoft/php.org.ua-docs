Повертає версію MySQL сервера

-   [« mysqli::$protocolversion](mysqli.get-proto-info.html)
    
-   [mysqli::$serverversion »](mysqli.get-server-version.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає версію MySQL сервера
    

# mysqli::$serverinfo

# mysqli::getserverinfo

# mysqligetserverinfo

(PHP 5, PHP 7, PHP 8)

mysqli::$serverinfo -- mysqli::getserverinfo -- mysqligetserverinfo — Повертає версію MySQL сервера

### Опис

Об'єктно-орієнтований стиль

string [$mysqli->serverinfo](mysqli.get-server-info.html)

```methodsynopsis
public mysqli_stmt::get_server_info(): string
```

Процедурний стиль

```methodsynopsis
mysqli_get_server_info(mysqli $mysql): string
```

Повертає рядок, що містить версію MySQL сервера, до якого також підключений модуль MySQLi.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Рядок символів, що містить версію сервера.

### Приклади

**Приклад #1 Приклад використання $mysqli->serverinfo**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password");

/* проверить соединение */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* вывести версию сервера */
printf("Версия сервера: %s\n", $mysqli->server_info);

/* закрыть соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password");

/* проверить соединение */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* вывести версию сервера */
printf("Версия сервера: %s\n", mysqli_get_server_info($link));

/* закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Server version: 4.1.2-alpha-debug
```

### Дивіться також

-   [mysqligetclientinfo()](mysqli.get-client-info.html) - Отримує інформацію про клієнта MySQL
-   [mysqligetclientversion()](mysqli.get-client-version.html) - Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqligetserverversion()](mysqli.get-server-version.html) - Повертає версію сервера MySQL, представлену у вигляді integer