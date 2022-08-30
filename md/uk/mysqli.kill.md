Запит для сервера завершити виконання процесу MySQL

-   [« mysqli::$insertід](mysqli.insert-id.html)
    
-   [mysqli::moreresults »](mysqli.more-results.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Запит для сервера завершити виконання процесу MySQL
    

# mysqli::kill

# mysqlikill

(PHP 5, PHP 7, PHP 8)

mysqli::kill -- mysqlikill — Запит для сервера завершити виконання MySQL

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::kill(int $process_id): bool
```

Процедурний стиль

```methodsynopsis
mysqli_kill(mysqli $mysql, int $process_id): bool
```

Ця функція використовується, щоб відправити на сервер команду завершити MySQL процес заданий параметром `process_id`. Значення цього параметра має бути отримано за допомогою функції [mysqlithreadid()](mysqli.thread-id.html)

Для завершення поточного запиту використовуйте SQL команду `KILL QUERY processid`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::kill()****

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* определим id нашего процесса */
$thread_id = $mysqli->thread_id;

/* убиваем соединение */
$mysqli->kill($thread_id);

/* здесь должна произойти ошибка */
if (!$mysqli->query("CREATE TABLE myCity LIKE City")) {
    printf("Ошибка: %s\n", $mysqli->error);
    exit;
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* определим id нашего процесса */
$thread_id = mysqli_thread_id($link);

/* убиваем соединение */
mysqli_kill($link, $thread_id);

/* здесь должна произойти ошибка */
if (!mysqli_query($link, "CREATE TABLE myCity LIKE City")) {
    printf("Ошибка: %s\n", mysqli_error($link));
    exit;
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Error: MySQL server has gone away
```

### Дивіться також

-   [mysqlithreadid()](mysqli.thread-id.html) - Повертає ID процесу поточного підключення