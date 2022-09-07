---
navigation:
  - mysqli.errno.md: '« mysqli::$errno'
  - mysqli.error.md: 'mysqli::$error »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$errorlist'
---
# mysqli::$errorlist

# mysqlierrorlist

(PHP 5> = 5.4.0, PHP 7, PHP 8)

mysqli::$errorlist - mysqlierrorlist — Повертає список помилок виконання останньої запущеної команди

### Опис

Об'єктно-орієнтований стиль

array [$mysqli->errorlist](mysqli.error-list.md)

Процедурний стиль

```methodsynopsis
mysqli_error_list(mysqli $mysql): array
```

Повертає масив помилок останнього виклику MySQLi, яка може завершувати роботу успіхом або невдачею.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Список помилок, кожна з яких представлена ​​асоціативним масивом (array) та містить номер помилки, її опис, а також код стану sqlstate.

### Приклади

**Приклад #1 Приклад використання $mysqli->errorlist**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "nobody", "");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if (!$mysqli->query("SET a=1")) {
    print_r($mysqli->error_list);
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if (!mysqli_query($link, "SET a=1")) {
    print_r(mysqli_error_list($link));
}

/* закрываем соединение */
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

-   [mysqliconnecterrno()](mysqli.connect-errno.md) - Повертає код помилки останньої спроби з'єднання
-   [mysqliconnecterror()](mysqli.connect-error.md) - Повертає опис останньої помилки підключення
-   [mysqlierror()](mysqli.error.md) - Повертає рядок із описом останньої помилки
-   [mysqlisqlstate()](mysqli.sqlstate.md) - Повертає код стану SQLSTATE останній MySQL операції
