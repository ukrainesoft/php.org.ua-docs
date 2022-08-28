Повертає список помилок виконання останньої запущеної команди

-   [« mysqli::$errno](mysqli.errno.html)
    
-   [mysqli::$error »](mysqli.error.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає список помилок виконання останньої запущеної команди
    

# mysqli::$errorlist

# mysqlierrorlist

(PHP 5> = 5.4.0, PHP 7, PHP 8)

mysqli::$errorlist - mysqlierrorlist — Повертає список помилок виконання останньої запущеної команди

### Опис

Об'єктно-орієнтований стиль

array [$mysqli->error\_list](mysqli.error-list.html)

Процедурний стиль

```methodsynopsis
mysqli_error_list(mysqli $mysql): array
```

Повертає масив помилок останнього виклику MySQLi, яка може завершувати роботу успіхом або невдачею.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

### Значення, що повертаються

Список помилок, кожна з яких представлена ​​асоціативним масивом (array) та містить номер помилки, її опис, а також код стану sqlstate.

### Приклади

**Приклад #1 Приклад використання $mysqli->errorlist**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "nobody", "");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if (!$mysqli->query("SET a=1")) {
    print_r($mysqli->error_list);
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if (!mysqli_query($link, "SET a=1")) {
    print_r(mysqli_error_list($link));
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Array
(
    [0] => Array
        (
            [errno] => 1193
            [sqlstate] => HY000
            [error] => Unknown system variable 'a'
        )

)
```

### Дивіться також

-   [mysqli\_connect\_errno()](mysqli.connect-errno.html) - Повертає код помилки останньої спроби з'єднання
-   [mysqli\_connect\_error()](mysqli.connect-error.html) - Повертає опис останньої помилки підключення
-   [mysqli\_error()](mysqli.error.html) - Повертає рядок із описом останньої помилки
-   [mysqli\_sqlstate()](mysqli.sqlstate.html) - Повертає код стану SQLSTATE останній MySQL операції