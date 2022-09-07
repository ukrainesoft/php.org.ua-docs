---
navigation:
  - mysqli.options.md: '« mysqli::options'
  - mysqli.poll.md: 'mysqli::poll »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::ping'
---
# mysqli::ping

# mysqliping

(PHP 5, PHP 7, PHP 8)

mysqli::ping -- mysqliping — Перевіряє працездатність з'єднання або намагається перепідключитися, якщо з'єднання розірвано

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::ping(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_ping(mysqli $mysql): bool
```

Перевіряє працездатність з'єднання із сервером. Якщо з'єднання розірвано, а глобальне налаштування [mysqli.reconnect](mysqli.configuration.md#ini.mysqli.reconnect) увімкнена, PHP спробує автоматично перепідключитися.

> **Зауваження**: Налаштування php.ini mysqli.reconnect ігнорується драйвером "mysqlnd", тому автоматичного перепідключення не відбудеться.

Ця функція може використовуватися клієнтами, які простоюють без діла довгий час, щоб перевірити, чи сервер їх не відключив, і перепідключитися у разі потреби.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::ping()****

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if ($mysqli->connect_errno) {
    printf("Не удалось подключиться: %s\n", $mysqli->connect_error);
    exit();
}

/* проверим, жив ли сервер */
if ($mysqli->ping()) {
    printf ("Соединение в порядке!\n");
} else {
    printf ("Ошибка: %s\n", $mysqli->error);
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

/* проверим, жив ли сервер */
if (mysqli_ping($link)) {
    printf ("Соединение в порядке!\n");
} else {
    printf ("Ошибка: %s\n", mysqli_error($link));
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Our connection is ok!
```
