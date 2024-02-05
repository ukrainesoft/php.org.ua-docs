---
navigation:
  - mysqli.get-host-info.md: '« mysqli::$host\_info'
  - mysqli.get-server-info.md: 'mysqli::$server\_info »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$protocol\_version'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$protocol\_version

# mysqli\_get\_proto\_info

(PHP 5, PHP 7, PHP 8)

mysqli::$protocol\_version -- mysqli\_get\_proto\_info — Повертає версію протоколу, що використовується MySQL

### Опис

Об'єктно-орієнтований стиль

int[$mysqli->protocol\_version](mysqli.get-proto-info.md)

Процедурний стиль

```methodsynopsis
mysqli_get_proto_info(mysqli $mysql): int
```

Повертає ціле число, що є версією протоколу MySQL, використовуваного для з'єднання, переданого в `mysql`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає ціле число, яке представляє версію протоколу.

### Приклади

**Приклад #1 Приклад використання $mysqli->protocol\_version**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password");

/* Вывести версию протокола */
printf("Версия протокола: %d\n", $mysqli->protocol_version);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password");

/* Вывести версию протокола */
printf("Версия протокола: %d\n", mysqli_get_proto_info($link));
?>
```

Результат виконання наведених прикладів:

```
Версия протокола: 10
```

### Дивіться також

-   [mysqli\_get\_host\_info()](mysqli.get-host-info.md) \- Повертає рядок, що містить тип використовуваної сполуки
