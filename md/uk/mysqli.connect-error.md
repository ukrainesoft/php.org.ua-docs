---
navigation:
  - mysqli.connect-errno.md: '« mysqli::$connecterrno'
  - mysqli.construct.md: 'mysqli::construct »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$connecterror'
---
# mysqli::$connecterror

# mysqliconnecterror

(PHP 5, PHP 7, PHP 8)

mysqli::$connecterror - mysqliconnecterror — Повертає опис останньої помилки підключення

### Опис

Об'єктно-орієнтований стиль

?string [$mysqli->connecterror](mysqli.connect-error.md)

Процедурний стиль

```methodsynopsis
mysqli_connect_error(): ?string
```

Повертає повідомлення про помилку останньої спроби підключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повідомлення про помилку . \*\*`null`\*\*якщо помилка відсутня.

### Приклади

**Приклад #1 Приклад використання $mysqli->connecterror**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_OFF);

/* @ используется для подавления предупреждений */
$mysqli = @new mysqli('localhost', 'fake_user', 'wrong_password', 'does_not_exist');

if ($mysqli->connect_error) {
    /* Используйте предпочитаемый вами метод регистрации ошибок */
    error_log('Ошибка при подключении: ' . $mysqli->connect_error);
}
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_OFF);

/* @ используется для подавления предупреждений */
$link = @mysqli_connect('localhost', 'fake_user', 'wrong_password', 'does_not_exist');

if (!$link) {
    /* Используйте предпочитаемый вами метод регистрации ошибок */
    error_log('Ошибка при подключении: ' . mysqli_connect_error());
}
?>
```

### Дивіться також

-   [mysqliconnect()](function.mysqli-connect.md) - Псевдонім mysqli::construct
-   [mysqliconnecterrno()](mysqli.connect-errno.md) - Повертає код помилки останньої спроби з'єднання
-   [mysqlierrno()](mysqli.errno.md) - Повертає код помилки останнього виклику функції
-   [mysqlierror()](mysqli.error.md) - Повертає рядок із описом останньої помилки
-   [mysqlisqlstate()](mysqli.sqlstate.md) - Повертає код стану SQLSTATE останній MySQL операції
