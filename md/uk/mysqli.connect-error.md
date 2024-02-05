---
navigation:
  - mysqli.connect-errno.md: '« mysqli::$connect\_errno'
  - mysqli.construct.md: 'mysqli::\_\_construct »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$connect\_error'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$connect\_error

# mysqli\_connect\_error

(PHP 5, PHP 7, PHP 8)

mysqli::$connect\_error -- mysqli\_connect\_error — Повертає опис останньої помилки підключення

### Опис

Об'єктно-орієнтований стиль

?string[$mysqli->connect\_error](mysqli.connect-error.md)

Процедурний стиль

```methodsynopsis
mysqli_connect_error(): ?string
```

Повертає повідомлення про помилку останньої спроби підключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Сообщение об ошибке\*\*`null`\*\*якщо помилка відсутня.

### Приклади

**Приклад #1 Приклад використання $mysqli->connect\_error**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_OFF);

/* @ используется для подавления предупреждений */
$mysqli = @new mysqli('localhost', 'fake_user', 'wrong_password', 'does_not_exist');

if ($mysqli->connect_error) {
    /* Используйте предпочитаемый вами метод регистрации ошибок */
    error_log('Ошибка при подключении: ' . $mysqli->connect_error);
}
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_OFF);

/* @ используется для подавления предупреждений */
$link = @mysqli_connect('localhost', 'fake_user', 'wrong_password', 'does_not_exist');

if (!$link) {
    /* Используйте предпочитаемый вами метод регистрации ошибок */
    error_log('Ошибка при подключении: ' . mysqli_connect_error());
}
?>
```

### Дивіться також

-   [mysqli\_connect()](function.mysqli-connect.md) \- Псевдонім mysqli::\_\_construct
-   [mysqli\_connect\_errno()](mysqli.connect-errno.md) \- Повертає код помилки останньої спроби з'єднання
-   [mysqli\_errno()](mysqli.errno.md) \- Повертає код помилки останнього виклику функції
-   [mysqli\_error()](mysqli.error.md) \- Повертає рядок із описом останньої помилки
-   [mysqli\_sqlstate()](mysqli.sqlstate.md) \- Повертає код стану SQLSTATE останній MySQL операції
