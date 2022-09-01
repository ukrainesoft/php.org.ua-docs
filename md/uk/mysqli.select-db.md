---
navigation:
  - mysqli.savepoint.md: '« mysqli::savepoint'
  - mysqli.set-charset.html: 'mysqli::setcharset »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::selectдб'
---
# mysqli::selectдб

# mysqliselectдб

(PHP 5, PHP 7, PHP 8)

mysqli::selectdb - mysqliselectdb — Встановлює базу даних для запитів, що виконуються.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::select_db(string $database): bool
```

Процедурний стиль

```methodsynopsis
mysqli_select_db(mysqli $mysql, string $database): bool
```

Встановлює базу даних, яка використовуватиметься під час виконання запитів до бази даних

> **Зауваження**
> 
> Ця функція використовується лише для зміни бази даних під час підключення. Ви можете вибрати базу даних, передавши її четвертим параметром функції [mysqliconnect()](function.mysqli-connect.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

`database`

Назва бази даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::selectdb()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

/* получаем имя текущей базы данных по умолчанию */
$result = $mysqli->query("SELECT DATABASE()");
$row = $result->fetch_row();
printf("База данных по умолчанию: %s.\n", $row[0]);

/* изменяем базу данных по умолчанию на "world" */
$mysqli->select_db("world");

/* получаем имя текущей базы данных по умолчанию */
$result = $mysqli->query("SELECT DATABASE()");
$row = $result->fetch_row();
printf("База данных по умолчанию: %s.\n", $row[0]);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

/* получаем имя текущей базы данных по умолчанию */
$result = mysqli_query($link, "SELECT DATABASE()");
$row = mysqli_fetch_row($result);
printf("База данных по умолчанию: %s.\n", $row[0]);

/* изменяем базу данных по умолчанию на "world" */
mysqli_select_db($link, "world");

/* получаем имя текущей базы данных по умолчанию */
$result = mysqli_query($link, "SELECT DATABASE()");
$row = mysqli_fetch_row($result);
printf("База данных по умолчанию: %s.\n", $row[0]);
```

Результат виконання даних прикладів:

```
База данных по умолчанию: test.
База данных по умолчанию: world.
```

### Дивіться також

-   [mysqliconnect()](function.mysqli-connect.md) - Псевдонім mysqli::construct
-   [mysqlirealconnect()](mysqli.real-connect.md) - Встановлює з'єднання із сервером mysql
