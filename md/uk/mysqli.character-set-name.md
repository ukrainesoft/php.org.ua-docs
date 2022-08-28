Повертає поточне кодування, встановлене для з'єднання з БД

-   [« mysqli::change\_user](mysqli.change-user.html)
    
-   [mysqli::close »](mysqli.close.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає поточне кодування, встановлене для з'єднання з БД
    

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

### Значення, що повертаються

Поточне кодування, встановлене для з'єднання

### Приклади

**Приклад #1 Приклад використання **mysqli::charactersetname()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Установка кодировки по умолчанию */
$mysqli->set_charset('utf8mb4');

/* Вывод текущей кодировки */
$charset = $mysqli->character_set_name();
printf("Текущая кодировка - %s\n", $charset);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Установка кодировки по умолчанию */
mysqli_set_charset($mysqli, 'utf8mb4');

/* Вывод текущей кодировки */
$charset = mysqli_character_set_name($mysqli);
printf("Текущая кодировка - %s\n", $charset);
```

Результат виконання даних прикладів:

```
Текущая кодировка - utf8mb4
```

### Дивіться також

-   [mysqli\_set\_charset()](mysqli.set-charset.html) - Встановлює набір символів
-   [mysqli\_real\_escape\_string()](mysqli.real-escape-string.html) - Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання