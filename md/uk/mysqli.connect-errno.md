---
navigation:
  - mysqli.commit.md: '« mysqli::commit'
  - mysqli.connect-error.md: 'mysqli::$connect\_error »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$connect\_errno'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$connect\_errno

# mysqli\_connect\_errno

(PHP 5, PHP 7, PHP 8)

mysqli::$connect\_errno -- mysqli\_connect\_errno — Повертає код помилки останньої спроби з'єднання.

### Опис

Об'єктно-орієнтований стиль

int[$mysqli->connect\_errno](mysqli.connect-errno.md)

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

**Приклад #1 Приклад використання $mysqli->connect\_errno**

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

-   [mysqli\_connect()](function.mysqli-connect.md) \- Псевдонім mysqli::\_\_construct
-   [mysqli\_connect\_error()](mysqli.connect-error.md) \- Повертає опис останньої помилки підключення
-   [mysqli\_errno()](mysqli.errno.md) \- Повертає код помилки останнього виклику функції
-   [mysqli\_error()](mysqli.error.md) \- Повертає рядок із описом останньої помилки
-   [mysqli\_sqlstate()](mysqli.sqlstate.md) \- Повертає код стану SQLSTATE останній MySQL операції
