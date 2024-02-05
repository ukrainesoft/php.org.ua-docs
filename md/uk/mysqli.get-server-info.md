---
navigation:
  - mysqli.get-proto-info.md: '« mysqli::$protocol\_version'
  - mysqli.get-server-version.md: 'mysqli::$server\_version »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$server\_info'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$server\_info

# mysqli::get\_server\_info

# mysqli\_get\_server\_info

(PHP 5, PHP 7, PHP 8)

mysqli::$server\_info -- mysqli::get\_server\_info -- mysqli\_get\_server\_info — Повертає версію MySQL сервера

### Опис

Об'єктно-орієнтований стиль

string[$mysqli->server\_info](mysqli.get-server-info.md)

```methodsynopsis
public mysqli_stmt::get_server_info(): string
```

Процедурний стиль

```methodsynopsis
mysqli_get_server_info(mysqli $mysql): string
```

Повертає рядок, що містить версію MySQL сервера, до якого також підключений модуль MySQLi.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Рядок символів, що містить версію сервера.

### Приклади

**Приклад #1 Приклад використання $mysqli->server\_info**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password");

/* выводим версию сервера */
printf("Версия сервера: %s\n", $mysqli->server_info);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password");

/* выводим версию сервера */
printf("Версия сервера: %s\n", mysqli_get_server_info($link));
?>
```

Результат виконання наведених прикладів:

```
Версия сервера: 8.0.21
```

### Дивіться також

-   [mysqli\_get\_client\_info()](mysqli.get-client-info.md) \- Отримує інформацію про клієнта MySQL
-   [mysqli\_get\_client\_version()](mysqli.get-client-version.md) \- Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqli\_get\_server\_version()](mysqli.get-server-version.md) \- Повертає версію сервера MySQL, представлену у вигляді integer
