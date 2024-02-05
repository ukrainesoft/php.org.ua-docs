---
navigation:
  - mysqli.get-server-info.md: '« mysqli::$server\_info'
  - mysqli.get-warnings.md: 'mysqli::get\_warnings »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$server\_version'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$server\_version

# mysqli\_get\_server\_version

(PHP 5, PHP 7, PHP 8)

mysqli::$server\_version -- mysqli\_get\_server\_version - Повертає версію сервера MySQL, представлену у вигляді integer

### Опис

Об'єктно-орієнтований стиль

int[$mysqli->server\_version](mysqli.get-server-version.md)

Процедурний стиль

```methodsynopsis
mysqli_get_server_version(mysqli $mysql): int
```

Функция**mysqli\_get\_server\_version()** повертає версію сервера, до якого створено з'єднання (передане у параметрі `mysql`) як цілого числа.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Цілочисельне представлення версії сервера.

Це число збирається так `main_version * 10000 + minor_version * 100 + sub_version`(т.е. версия 4.1.0 будет представлена как 40100).

### Приклади

**Приклад #1 Приклад використання $mysqli->server\_version**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password");

/* выводим версию сервера */
printf("Версия сервера: %d\n", $mysqli->server_version);
?>
```

Процедурний стиль

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password");

/* выводим версию сервера */
printf("Версия сервера: %d\n", mysqli_get_server_version($link));
?>
```

Результат виконання наведених прикладів:

```
Версия сервера: 80021
```

### Дивіться також

-   [mysqli\_get\_client\_info()](mysqli.get-client-info.md) \- Отримує інформацію про клієнта MySQL
-   [mysqli\_get\_client\_version()](mysqli.get-client-version.md) \- Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqli\_get\_server\_info()](mysqli.get-server-info.md) \- Повертає версію MySQL сервера
