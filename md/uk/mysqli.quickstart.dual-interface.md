---
navigation:
  - mysqli.quickstart.md: « Краткое руководство
  - mysqli.quickstart.connections.md: Соединения »
  - index.md: PHP Manual
  - mysqli.quickstart.md: Краткое руководство
title: Процедурний та об'єктно-орієнтований інтерфейс
---
## Процедурний та об'єктно-орієнтований інтерфейс

Модуль mysqli надає подвійний інтерфейс програмісту. Підтримуються як процедурна, і об'єктно-орієнтована парадигми програмування.

Користувачі, що переходять зі старого модуля mysql, можливо, віддадуть перевагу процедурному інтерфейсу. Він дуже схожий на інтерфейс старого модуля, і в багатьох випадках функції відрізняються тільки префіксом в імені. Деякі mysqli-функції приймають дескриптор з'єднання першим аргументом, на відміну від відповідних їм функцій старого модуля, які приймають його як останній необов'язковий аргумент.

**Приклад #1 Простота переходу зі старого модуля mysql**

```php
<?php
$mysqli = mysqli_connect("example.com", "user", "password", "database");
$result = mysqli_query($mysqli, "SELECT 'Пожалуйста, не используйте устаревший модуль mysql в новых проектах.' AS _msg FROM DUAL");
$row = mysqli_fetch_assoc($result);
echo $row['_msg'];

$mysql = mysql_connect("example.com", "user", "password");
mysql_select_db("test");
$result = mysql_query("SELECT 'Используйте вместо него модуль mysqli.' AS _msg FROM DUAL", $mysql);
$row = mysql_fetch_assoc($result);
echo $row['_msg'];
?>
```

Результат виконання цього прикладу:

```
Пожалуйста, не используйте устаревший модуль mysql в новых проектах. Используйте вместо него модуль mysqli.
```

*Об'єктно-орієнтований інтерфейс*

На додаток до процедурного, користувачі можуть використовувати об'єктно-орієнтований інтерфейс. Документацію заточено саме під об'єктний інтерфейс. Об'єктно-орієнтований інтерфейс пропонує функції згруповані за метою їх застосування, що полегшує їх пошук і освоєння. Тим не менш, у практичних прикладах до функцій наводиться код для обох парадигм.

Якихось принципових відмінностей у продуктивності між інтерфейсами немає. Користувачі вільні у виборі інтерфейсу, ґрунтуючись на особистих уподобаннях.

**Приклад #2 Об'єктно-орієнтований та процедурний інтерфейси**

```php
<?php

$mysqli = mysqli_connect("example.com", "user", "password", "database");

$result = mysqli_query($mysqli, "SELECT 'Мир, полный ' AS _msg FROM DUAL");
$row = mysqli_fetch_assoc($result);
echo $row['_msg'];

$mysqli = new mysqli("example.com", "user", "password", "database");

$result = $mysqli->query("SELECT 'выбора, чтобы угодить всем.' AS _msg FROM DUAL");
$row = $result->fetch_assoc();
echo $row['_msg'];
```

Результат виконання цього прикладу:

```
Мир, полный выбора, чтобы угодить всем.
```

Приклади в цьому посібнику будуть написані в об'єктному стилі через те, що об'єктному підходу віддавалася перевага при створенні документації.

*Змішування стилів*

Перемикатися між стилями програмування можна як завгодно часто і в будь-який час, проте робити цього не рекомендується, так як це погіршує читання коду і ускладнює його підтримку.

**Приклад #3 Поганий стиль програмування**

```php
<?php

$mysqli = new mysqli("example.com", "user", "password", "database");

$result = mysqli_query($mysqli, "SELECT 'Этот код работает, но лучше так не писать.' AS _msg FROM DUAL");

if ($row = $result->fetch_assoc()) {
    echo $row['_msg'];
}
```

Результат виконання цього прикладу:

```
Этот код работает, но лучше так не писать.
```

*Дивіться також*

-   [mysqli::construct()](mysqli.construct.md)
-   [mysqli::query()](mysqli.query.md)
-   [mysqliresult::fetchassoc()](mysqli-result.fetch-assoc.md)
-   [$mysqli::connecterrno](mysqli.connect-errno.md)
-   [$mysqli::connecterror](mysqli.connect-error.md)
-   [$mysqli::errno](mysqli.errno.md)
-   [$mysqli::error](mysqli.error.md)
-   [Общее описание функций модуля MySQLi](mysqli.summary.md)
