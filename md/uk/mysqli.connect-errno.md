---
navigation:
  - mysqli.commit.md: '« mysqli::commit'
  - mysqli.connect-error.md: 'mysqli::$connecterror »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$connecterrno'
---
# mysqli::$connecterrno

# mysqliconnecterrno

(PHP 5, PHP 7, PHP 8)

mysqli::$connecterrno - mysqliconnecterrno — Повертає код помилки останньої спроби з'єднання.

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->connecterrno](mysqli.connect-errno.md)

Процедурний стиль

```methodsynopsis
mysqli_connect_errno(): int
```

Повернення коду помилки останньої спроби підключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Код помилки останньої спроби підключення. За відсутності помилок виводить 0.

### Приклади

**Приклад #1 Приклад використання $mysqli->connecterrno**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_OFF);

/* @ используется для подавления предупреждений */
$mysqli = @new mysqli('localhost', 'fake_user', 'wrong_password', 'does_not_exist');

if ($mysqli->connect_errno) {
    /* Используйте предпочитаемый вами метод регистрации ошибок */
    error_log('Ошибка соединения: ' . $mysqli->connect_errno);
}
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_OFF);

/* @ is used to suppress warnings */
$link = @mysqli_connect('localhost', 'fake_user', 'wrong_password', 'does_not_exist');

if (!$link) {
    /* Используйте предпочитаемый вами метод регистрации ошибок */
    error_log('Ошибка соединения: ' . mysqli_connect_errno());
}
?>
```

### Дивіться також

-   [mysqliconnect()](function.mysqli-connect.md) - Псевдонім mysqli::construct
-   [mysqliconnecterror()](mysqli.connect-error.md) - Повертає опис останньої помилки підключення
-   [mysqlierrno()](mysqli.errno.md) - Повертає код помилки останнього виклику функції
-   [mysqlierror()](mysqli.error.md) - Повертає рядок із описом останньої помилки
-   [mysqlisqlstate()](mysqli.sqlstate.md) - Повертає код стану SQLSTATE останній MySQL операції
