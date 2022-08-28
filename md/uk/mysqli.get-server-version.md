Повертає версію сервера MySQL, представлену у вигляді integer

-   [« mysqli::$server\_info](mysqli.get-server-info.html)
    
-   [mysqli::get\_warnings »](mysqli.get-warnings.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає версію сервера MySQL, представлену у вигляді integer
    

# mysqli::$serverversion

# mysqligetserverversion

(PHP 5, PHP 7, PHP 8)

mysqli::$serverversion -- mysqligetserverversion - Повертає версію сервера MySQL, представлену у вигляді integer

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->server\_version](mysqli.get-server-version.html)

Процедурний стиль

```methodsynopsis
mysqli_get_server_version(mysqli $mysql): int
```

Функція **mysqligetserverversion()** повертає версію сервера, до якого створено з'єднання (передане у параметрі `mysql`) як цілого числа.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

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

-   [mysqli\_get\_client\_info()](mysqli.get-client-info.html) - Отримує інформацію про клієнта MySQL
-   [mysqli\_get\_client\_version()](mysqli.get-client-version.html) - Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqli\_get\_server\_info()](mysqli.get-server-info.html) - Повертає версію MySQL сервера