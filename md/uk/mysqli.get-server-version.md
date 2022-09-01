---
navigation:
  - mysqli.get-server-info.html: '« mysqli::$serverinfo'
  - mysqli.get-warnings.html: 'mysqli::getwarnings »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$serverversion'
---
# mysqli::$serverversion

# mysqligetserverversion

(PHP 5, PHP 7, PHP 8)

mysqli::$serverversion -- mysqligetserverversion - Повертає версію сервера MySQL, представлену у вигляді integer

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->serverversion](mysqli.get-server-version.html)

Процедурний стиль

```methodsynopsis
mysqli_get_server_version(mysqli $mysql): int
```

Функція **mysqligetserverversion()** повертає версію сервера, до якого створено з'єднання (передане у параметрі `mysql`) як цілого числа.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Цілочисельне представлення версії сервера.

Це число збирається так `main_version * 10000 + minor_version * 100 + sub_version` (Тобто версія 4.1.0 буде представлена ​​як 40100).

### Приклади

**Приклад #1 Приклад використання $mysqli->serverversion**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Соединение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* выводим версию сервера */
printf("Версия сервера: %d\n", $mysqli->server_version);

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Соединение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* выводим версию сервера */
printf("Версия сервера: %d\n", mysqli_get_server_version($link));

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Версия сервера: 40102
```

### Дивіться також

-   [mysqligetclientinfo()](mysqli.get-client-info.html) - Отримує інформацію про клієнта MySQL
-   [mysqligetclientversion()](mysqli.get-client-version.html) - Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqligetserverinfo()](mysqli.get-server-info.html) - Повертає версію MySQL сервера
