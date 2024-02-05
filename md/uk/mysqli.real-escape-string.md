---
navigation:
  - mysqli.real-connect.md: '« mysqli::real\_connect'
  - mysqli.real-query.md: 'mysqli::real\_query »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::real\_escape\_string'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::real\_escape\_string

# mysqli::escape\_string

# mysqli\_real\_escape\_string

(PHP 5, PHP 7, PHP 8)

mysqli::real\_escape\_string -- mysqli::escape\_string -- mysqli\_real\_escape\_string — Екран спеціальних символів у рядку для використання в SQL-вираженні, використовуючи поточний набір символів з'єднання

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::real_escape_string(string $string): string
```

Процедурний стиль

```methodsynopsis
mysqli_real_escape_string(mysqli $mysql, string $string): string
```

Ця функція використовується для створення допустимих SQL рядків, які можна використовувати в SQL виразах. Цей рядок кодується для створення екранованого рядка SQL з урахуванням поточного набору символів підключення.

**Застереження**

# Безпека: набір символів за промовчанням

Набір символів повинен бути заданий на стороні сервера, або за допомогою API-функції [mysqli\_set\_charset()](mysqli.set-charset.md). В іншому випадку **mysqli\_real\_escape\_string()** працювати не буде. За додатковою інформацією звертайтесь до документації [набори символів](mysqlinfo.concepts.charset.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`string`

Рядок, який потрібно екранувати.

Екрановані символи `NUL (ASCII 0)` `\n` `\r` `\` `'` `"`и CTRL+Z.

### Значення, що повертаються

Повертає екранований рядок.

### Приклади

**Приклад #1 Приклад використання** mysqli::real\_escape\_string()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$city = "'s-Hertogenbosch";

/* этот запрос с экранированным $city будет работать */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'",
    $mysqli->real_escape_string($city));
$result = $mysqli->query($query);
printf("Возвращённые строки: %d.\n", $result->num_rows);

/* этот запрос завершится ошибкой, потому что мы не экранировали $city */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'", $city);
$result = $mysqli->query($query);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$city = "'s-Hertogenbosch";

/* этот запрос с экранированным $city будет работать */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'",
    mysqli_real_escape_string($mysqli, $city));
$result = mysqli_query($mysqli, $query);
printf("Возвращённые строки: %d.\n", mysqli_num_rows($result));

/* этот запрос завершится ошибкой, потому что мы не экранировали $city */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'", $city);
$result = mysqli_query($mysqli, $query);
```

Висновок наведених прикладів буде схожим на:

```
Возвращённые строки: 1.

Fatal error: Uncaught mysqli_sql_exception: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 's-Hertogenbosch'' at line 1 in...
```

### Дивіться також

-   [mysqli\_set\_charset()](mysqli.set-charset.md) \- Встановлює набір символів
