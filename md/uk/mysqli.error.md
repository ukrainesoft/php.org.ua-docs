---
navigation:
  - mysqli.error-list.md: '« mysqli::$error\_list'
  - mysqli.execute-query.md: 'mysqli::execute\_query »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$error'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$error

# mysqli\_error

(PHP 5, PHP 7, PHP 8)

mysqli::$error -- mysqli\_error — Повертає рядок із описом останньої помилки

### Опис

Об'єктно-орієнтований стиль

string[$mysqli->error](mysqli.error.md)

Процедурний стиль

```methodsynopsis
mysqli_error(mysqli $mysql): string
```

Повертає повідомлення про помилку останнього виклику MySQLi, який може успішно виконатися або провалитися.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Рядок з описом помилки. Порожній рядок, якщо помилок немає.

### Приклади

**Приклад #1 Приклад $mysqli->error**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if ($mysqli->connect_errno) {
    printf("Соединение не удалось: %s\n", $mysqli->connect_error);
    exit();
}

if (!$mysqli->query("SET a=1")) {
    printf("Сообщение ошибки: %s\n", $mysqli->error);
}

/* Закрыть соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Соединение не удалось: %s\n", mysqli_connect_error());
    exit();
}

if (!mysqli_query($link, "SET a=1")) {
    printf("Сообщение ошибки: %s\n", mysqli_error($link));
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Сообщение ошибки: Unknown system variable 'a'
```

### Дивіться також

-   [mysqli\_connect\_errno()](mysqli.connect-errno.md) \- Повертає код помилки останньої спроби з'єднання
-   [mysqli\_connect\_error()](mysqli.connect-error.md) \- Повертає опис останньої помилки підключення
-   [mysqli\_errno()](mysqli.errno.md) \- Повертає код помилки останнього виклику функції
-   [mysqli\_sqlstate()](mysqli.sqlstate.md) \- Повертає код стану SQLSTATE останній MySQL операції
