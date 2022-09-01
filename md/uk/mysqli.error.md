---
navigation:
  - mysqli.error-list.html: '« mysqli::$errorlist'
  - mysqli.field-count.html: 'mysqli::$fieldcount »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$error'
---
# mysqli::$error

# mysqlierror

(PHP 5, PHP 7, PHP 8)

mysqli::$error -- mysqlierror — Повертає рядок із описом останньої помилки

### Опис

Об'єктно-орієнтований стиль

string [$mysqli->error](mysqli.error.md)

Процедурний стиль

```methodsynopsis
mysqli_error(mysqli $mysql): string
```

Повертає повідомлення про помилку останнього виклику MySQLi, який може успішно виконатися або провалитися.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Рядок з описом помилки. Порожній рядок, якщо помилок немає.

### Приклади

**Приклад #1 Приклад $mysqli->error**

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
    printf("Сообщение ошибки: %s\n", $mysqli->error);
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
    printf("Сообщение ошибки: %s\n", mysqli_error($link));
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Сообщение ошибки: Unknown system variable 'a'
```

### Дивіться також

-   [mysqliconnecterrno()](mysqli.connect-errno.html) - Повертає код помилки останньої спроби з'єднання
-   [mysqliconnecterror()](mysqli.connect-error.html) - Повертає опис останньої помилки підключення
-   [mysqlierrno()](mysqli.errno.md) - Повертає код помилки останнього виклику функції
-   [mysqlisqlstate()](mysqli.sqlstate.md) - Повертає код стану SQLSTATE останній MySQL операції
