---
navigation:
  - mysqli.savepoint.md: '« mysqli::savepoint'
  - mysqli.set-charset.md: 'mysqli::set\_charset »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::select\_db'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::select\_db

# mysqli\_select\_db

(PHP 5, PHP 7, PHP 8)

mysqli::select\_db -- mysqli\_select\_db — Встановлює базу даних для запитів, що виконуються.

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

> **Зауваження** :
> 
> Ця функція використовується лише для зміни бази даних під час підключення. Ви можете вибрати базу даних, передавши її четвертим параметром функції [mysqli\_connect()](function.mysqli-connect.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`database`

Назва бази даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Пример #1 Пример использования**mysqli::select\_db()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

/* получаем имя текущей базы данных по умолчанию */
$result = $mysqli->query("SELECT DATABASE()");
$row = $result->fetch_row();
printf("База данных по умолчанию: %s.\n", $row[0]);

/* изменяем базу данных по умолчанию на "world" */
$mysqli->select_db("world");

/* получаем имя текущей базы данных по умолчанию */
$result = $mysqli->query("SELECT DATABASE()");
$row = $result->fetch_row();
printf("База данных по умолчанию: %s.\n", $row[0]);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

/* получаем имя текущей базы данных по умолчанию */
$result = mysqli_query($link, "SELECT DATABASE()");
$row = mysqli_fetch_row($result);
printf("База данных по умолчанию: %s.\n", $row[0]);

/* изменяем базу данных по умолчанию на "world" */
mysqli_select_db($link, "world");

/* получаем имя текущей базы данных по умолчанию */
$result = mysqli_query($link, "SELECT DATABASE()");
$row = mysqli_fetch_row($result);
printf("База данных по умолчанию: %s.\n", $row[0]);
```

Результат виконання наведених прикладів:

```
База данных по умолчанию: test.
База данных по умолчанию: world.
```

### Дивіться також

-   [mysqli\_connect()](function.mysqli-connect.md) \- Псевдонім mysqli::\_\_construct
-   [mysqli\_real\_connect()](mysqli.real-connect.md) \- Встановлює з'єднання із сервером mysql
