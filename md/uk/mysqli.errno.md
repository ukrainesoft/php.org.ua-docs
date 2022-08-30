Повертає код помилки останнього виклику функції

-   [« mysqli::dumpdebuginfo](mysqli.dump-debug-info.html)
    
-   [mysqli::$errorlist »](mysqli.error-list.html)
    
-   [PHP Manual](index.md)
    
-   [mysqli](class.mysqli.md)
    
-   Повертає код помилки останнього виклику функції
    

# mysqli::$errno

# mysqlierrno

(PHP 5, PHP 7, PHP 8)

mysqli::$errno -- mysqlierrno — Повернення коду помилки останнього виклику функції

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->errno](mysqli.errno.md)

Процедурний стиль

```methodsynopsis
mysqli_errno(mysqli $mysql): int
```

Повертає код помилки останнього виклику MySQLi, що завершилася успішним виконанням або помилкою.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Код помилки останнього виклику функції у разі провалу. За відсутності помилок виводить 0.

### Приклади

**Приклад #1 Приклад використання $mysqli->errno**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if ($mysqli->connect_errno) {
    printf("Соединение не удалось: %s\n", $mysqli->connect_error);
    exit();
}

if (!$mysqli->query("SET a=1")) {
    printf("Код ошибки: %d\n", $mysqli->errno);
}

/* Закрыть соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Соединение не удалось: %s\n", mysqli_connect_error());
    exit();
}

if (!mysqli_query($link, "SET a=1")) {
    printf("Код ошибки: %d\n", mysqli_errno($link));
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Код ошибки: 1193
```

### Дивіться також

-   [mysqliconnecterrno()](mysqli.connect-errno.html) - Повертає код помилки останньої спроби з'єднання
-   [mysqliconnecterror()](mysqli.connect-error.html) - Повертає опис останньої помилки підключення
-   [mysqlierror()](mysqli.error.md) - Повертає рядок із описом останньої помилки
-   [mysqlisqlstate()](mysqli.sqlstate.md) - Повертає код стану SQLSTATE останній MySQL операції