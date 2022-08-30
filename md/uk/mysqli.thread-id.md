Повертає ID процесу поточного підключення

-   [« mysqli::storeresult](mysqli.store-result.html)
    
-   [mysqli::threadsafe »](mysqli.thread-safe.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає ID процесу поточного підключення
    

# mysqli::$threadід

# mysqlithreadід

(PHP 5, PHP 7, PHP 8)

mysqli::$threadid - mysqlithreadid — Повертає ID процесу поточного підключення

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->threadід](mysqli.thread-id.html)

Процедурний стиль

```methodsynopsis
mysqli_thread_id(mysqli $mysql): int
```

**mysqlithreadid()** повертає ID процесу поточного підключення, який можна завершити функцією [mysqlikill()](mysqli.kill.html). Якщо з'єднання було розірвано та відновлено функцією [mysqliping()](mysqli.ping.html), ID процесу буде вже іншим. Тому потрібно отримувати цей ідентифікатор, коли це справді необхідно.

> **Зауваження**
> 
> ID процесу призначається за принципом підключення-за-підключенням. Відповідно, якщо з'єднання розірвано та заново встановлено, йому буде присвоєно новий ідентифікатор.
> 
> Для завершення запущеного запиту можна використовувати SQL-команду `KILL QUERY processid`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Повертає ID процесу поточного з'єднання.

### Приклади

**Приклад #1 Приклад використання $mysqli->threadід**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* определяем наш id процесса */
$thread_id = $mysqli->thread_id;

/* убиваем соединение */
$mysqli->kill($thread_id);

/* тут должна произойти ошибка */
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

/* определяем наш id процесса */
$thread_id = mysqli_thread_id($link);

/* убиваем соединение */
mysqli_kill($link, $thread_id);

/* тут должна произойти ошибка */
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
Ошибка: MySQL server has gone away
```

### Дивіться також

-   [mysqlikill()](mysqli.kill.html) - Запит для сервера завершити виконання процесу MySQL