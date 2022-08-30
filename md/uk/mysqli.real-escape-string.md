Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання

-   [« mysqli::realconnect](mysqli.real-connect.html)
    
-   [mysqli::realquery »](mysqli.real-query.html)
    
-   [PHP Manual](index.md)
    
-   [mysqli](class.mysqli.md)
    
-   Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання
    

# mysqli::realescapestring

# mysqli::escapestring

# mysqlirealescapestring

(PHP 5, PHP 7, PHP 8)

mysqli::realescapestring -- mysqli::escapestring -- mysqlirealescapestring — Екран спеціальних символів у рядку для використання в SQL-вираженні, використовуючи поточний набір символів з'єднання

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

Набір символів повинен бути заданий на стороні сервера, або за допомогою API-функції [mysqlisetcharset()](mysqli.set-charset.html). В іншому випадку **mysqlirealescapestring()** працювати не буде. За додатковою інформацією звертайтесь до документації [набори символів](mysqlinfo.concepts.charset.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

`string`

Рядок, який потрібно екранувати.

Екрановані символи `NUL (ASCII 0), \n, \r, \, ', ", и Control-Z`

### Значення, що повертаються

Повертає екранований рядок.

### Приклади

**Приклад #1 Приклад використання **mysqli::realescapestring()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$city = "'s-Hertogenbosch";

/* этот запрос с экранированным $city будет работать */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'",
    $mysqli->real_escape_string($city));
$result = $mysqli->query($query);
printf("Возвращённые строки: %d.\n", $result->num_rows);

/* этот запрос завершится ошибкой, потому что мы не экранировали $city */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'", $city);
$result = $mysqli->query($query);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$city = "'s-Hertogenbosch";

/* этот запрос с экранированным $city будет работать */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'",
    mysqli_real_escape_string($mysqli, $city));
$result = mysqli_query($mysqli, $query);
printf("Возвращённые строки: %d.\n", mysqli_num_rows($result));

/* этот запрос завершится ошибкой, потому что мы не экранировали $city */
$query = sprintf("SELECT CountryCode FROM City WHERE name='%s'", $city);
$result = mysqli_query($mysqli, $query);
```

Результатом виконання даних прикладів буде щось подібне:

```
Возвращённые строки: 1.

Fatal error: Uncaught mysqli_sql_exception: You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 's-Hertogenbosch'' at line 1 in...
```

### Дивіться також

-   [mysqlisetcharset()](mysqli.set-charset.html) - Встановлює набір символів