---
navigation:
  - mysqli.get-connection-stats.html: '« mysqli::getconnectionstats'
  - mysqli.get-proto-info.html: 'mysqli::$protocolversion »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
title: 'mysqli::$hostinfo'
---
# mysqli::$hostinfo

# mysqligethostinfo

(PHP 5, PHP 7, PHP 8)

mysqli::$hostinfo -- mysqligethostinfo — Повертає рядок, що містить тип використовуваного з'єднання

### Опис

Об'єктно-орієнтований стиль

string [$mysqli->hostinfo](mysqli.get-host-info.html)

Процедурний стиль

```methodsynopsis
mysqli_get_host_info(mysqli $mysql): string
```

Повертає рядок, який описує з'єднання, яке позначено у параметрі `mysql` (включаючи ім'я сервера).

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Символьний рядок, що містить ім'я сервера хоста і тип підключення.

### Приклади

**Приклад #1 Приклад використання $mysqli->hostinfo**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* вывод информации о хосте */
printf("Информация о хосте: %s\n", $mysqli->host_info);

/* закрытие соединения */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* вывод информации о хосте */
printf("Информация о хосте: %s\n", mysqli_get_host_info($link));

/* закрытие соединения */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Информация о хосте: Localhost via UNIX socket
```

### Дивіться також

-   [mysqligetprotoinfo()](mysqli.get-proto-info.html) - Повертає версію використовуваного MySQL протоколу
