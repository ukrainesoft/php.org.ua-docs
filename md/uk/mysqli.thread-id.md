---
navigation:
  - mysqli.store-result.md: '« mysqli::store\_result'
  - mysqli.thread-safe.md: 'mysqli::thread\_safe »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$thread\_id'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$thread\_id

# mysqli\_thread\_id

(PHP 5, PHP 7, PHP 8)

mysqli::$thread\_id -- mysqli\_thread\_id — Повертає ID процесу поточного підключення

### Опис

Об'єктно-орієнтований стиль

int[$mysqli->thread\_id](mysqli.thread-id.md)

Процедурний стиль

```methodsynopsis
mysqli_thread_id(mysqli $mysql): int
```

**mysqli\_thread\_id()** повертає ID процесу поточного підключення, який можна завершити функцією [mysqli\_kill()](mysqli.kill.md). Якщо з'єднання було розірвано та відновлено функцією [mysqli\_ping()](mysqli.ping.md), ID процесу буде вже іншим. Тому потрібно отримувати цей ідентифікатор, коли це справді необхідно.

> **Зауваження** :
> 
> ID процесу призначається за принципом підключення-за-підключенням. Відповідно, якщо з'єднання розірвано та заново встановлено, йому буде присвоєно новий ідентифікатор.
> 
> Для завершення запущеного запиту можна використовувати SQL-команду `KILL QUERY processid`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає ID процесу поточного з'єднання.

### Приклади

**Приклад #1 Приклад використання $mysqli->thread\_id**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* определяем наш id процесса */
$thread_id = $mysqli->thread_id;

/* убиваем соединение */
$mysqli->kill($thread_id);

/* тут должна произойти ошибка */
if (!$mysqli->query("CREATE TABLE myCity LIKE City")) {
    printf("Ошибка: %s\n", $mysqli->error);
    exit;
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* определяем наш id процесса */
$thread_id = mysqli_thread_id($link);

/* убиваем соединение */
mysqli_kill($link, $thread_id);

/* тут должна произойти ошибка */
if (!mysqli_query($link, "CREATE TABLE myCity LIKE City")) {
    printf("Ошибка: %s\n", mysqli_error($link));
    exit;
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Ошибка: MySQL server has gone away
```

### Дивіться також

-   [mysqli\_kill()](mysqli.kill.md) \- Запит для сервера завершити виконання процесу MySQL
