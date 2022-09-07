---
navigation:
  - mysqli.change-user.md: '« mysqli::changeuser'
  - mysqli.close.md: 'mysqli::close »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::charactersetname'
---
# mysqli::charactersetname

# mysqlicharactersetname

(PHP 5, PHP 7, PHP 8)

mysqli::charactersetname -- mysqlicharactersetname — Повертає поточне кодування, встановлене для підключення до БД.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::character_set_name(): string
```

Процедурний стиль

```methodsynopsis
mysqli_character_set_name(mysqli $mysql): string
```

Повертає поточне кодування, встановлене для з'єднання з БД.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Поточне кодування, встановлене для з'єднання

### Приклади

**Приклад #1 Приклад використання **mysqli::charactersetname()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Установка кодировки по умолчанию */
$mysqli->set_charset('utf8mb4');

/* Вывод текущей кодировки */
$charset = $mysqli->character_set_name();
printf("Текущая кодировка - %s\n", $charset);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Установка кодировки по умолчанию */
mysqli_set_charset($mysqli, 'utf8mb4');

/* Вывод текущей кодировки */
$charset = mysqli_character_set_name($mysqli);
printf("Текущая кодировка - %s\n", $charset);
```

Результат виконання даних прикладів:

```
Текущая кодировка - utf8mb4
```

### Дивіться також

-   [mysqlisetcharset()](mysqli.set-charset.md) - Встановлює набір символів
-   [mysqlirealescapestring()](mysqli.real-escape-string.md) - Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання
