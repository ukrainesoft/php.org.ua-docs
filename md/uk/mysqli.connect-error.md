Повертає опис останньої помилки підключення

-   [« mysqli::$connect\_errno](mysqli.connect-errno.html)
    
-   [mysqli::\_\_construct »](mysqli.construct.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає опис останньої помилки підключення
    

# mysqli::$connecterror

# mysqliconnecterror

(PHP 5, PHP 7, PHP 8)

mysqli::$connecterror - mysqliconnecterror — Повертає опис останньої помилки підключення

### Опис

Об'єктно-орієнтований стиль

?string [$mysqli->connect\_error](mysqli.connect-error.html)

Процедурний стиль

```methodsynopsis
mysqli_connect_error(): ?string
```

Повертає повідомлення про помилку останньої спроби підключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повідомлення про помилку . **`null`**якщо помилка відсутня.

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

-   [mysqli\_connect()](function.mysqli-connect.html) - Псевдонім mysqli::construct
-   [mysqli\_connect\_errno()](mysqli.connect-errno.html) - Повертає код помилки останньої спроби з'єднання
-   [mysqli\_errno()](mysqli.errno.html) - Повертає код помилки останнього виклику функції
-   [mysqli\_error()](mysqli.error.html) - Повертає рядок із описом останньої помилки
-   [mysqli\_sqlstate()](mysqli.sqlstate.html) - Повертає код стану SQLSTATE останній MySQL операції