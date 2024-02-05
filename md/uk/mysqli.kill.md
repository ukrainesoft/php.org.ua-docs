---
navigation:
  - mysqli.insert-id.md: '« mysqli::$insert\_id'
  - mysqli.more-results.md: 'mysqli::more\_results »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::kill'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::kill

# mysqli\_kill

(PHP 5, PHP 7, PHP 8)

mysqli::kill -- mysqli\_kill — Запит для сервера завершити виконання MySQL

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::kill(int $process_id): bool
```

Процедурний стиль

```methodsynopsis
mysqli_kill(mysqli $mysql, int $process_id): bool
```

Ця функція використовується, щоб відправити на сервер команду завершити MySQL процес заданий параметром `process_id`. Значення цього параметра має бути отримано за допомогою функції [mysqli\_thread\_id()](mysqli.thread-id.md)

Для завершення поточного запиту використовуйте SQL команду `KILL QUERY processid`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Пример #1 Пример использования**mysqli::kill()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* определим id нашего процесса */
$thread_id = $mysqli->thread_id;

/* убиваем соединение */
$mysqli->kill($thread_id);

/* здесь должна произойти ошибка */
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

/* определим id нашего процесса */
$thread_id = mysqli_thread_id($link);

/* убиваем соединение */
mysqli_kill($link, $thread_id);

/* здесь должна произойти ошибка */
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
Error: MySQL server has gone away
```

### Дивіться також

-   [mysqli\_thread\_id()](mysqli.thread-id.md) \- Повертає ID процесу поточного підключення
