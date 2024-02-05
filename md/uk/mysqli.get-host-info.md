---
navigation:
  - mysqli.get-connection-stats.md: '« mysqli::get\_connection\_stats'
  - mysqli.get-proto-info.md: 'mysqli::$protocol\_version »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$host\_info'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$host\_info

# mysqli\_get\_host\_info

(PHP 5, PHP 7, PHP 8)

mysqli::$host\_info -- mysqli\_get\_host\_info — Повертає рядок, що містить тип використовуваного з'єднання

### Опис

Об'єктно-орієнтований стиль

string[$mysqli->host\_info](mysqli.get-host-info.md)

Процедурний стиль

```methodsynopsis
mysqli_get_host_info(mysqli $mysql): string
```

Повертає рядок, що описує з'єднання, яке позначено у параметрі `mysql`(включая имя хоста сервера).

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Символьний рядок, що містить ім'я сервера хоста і тип підключення.

### Приклади

**Приклад #1 Приклад використання $mysqli->host\_info**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* вывод информации о хосте */
printf("Информация о хосте: %s\n", $mysqli->host_info);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* вывод информации о хосте */
printf("Информация о хосте: %s\n", mysqli_get_host_info($link));
?>
```

Результат виконання наведених прикладів:

```
Информация о хосте: Localhost via UNIX socket
```

### Дивіться також

-   [mysqli\_get\_proto\_info()](mysqli.get-proto-info.md) \- Повертає версію використовуваного MySQL протоколу
