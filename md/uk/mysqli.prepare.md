---
navigation:
  - mysqli.poll.md: '« mysqli::poll'
  - mysqli.query.md: 'mysqli::query »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::prepare'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::prepare

# mysqli\_prepare

(PHP 5, PHP 7, PHP 8)

mysqli::prepare -- mysqli\_prepare — Підготовляє SQL вираз до виконання

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::prepare(string $query): mysqli_stmt|false
```

Процедурний стиль

```methodsynopsis
mysqli_prepare(mysqli $mysql, string $query): mysqli_stmt|false
```

Підготовляє SQL-запит і повертає покажчик цього виразу, який можна використовувати подальших операцій із цим виразом. Запит повинен складатися з одного виразу SQL.

Шаблон оператора може містити нуль або кілька знаків запитання (`?` ), позначок параметрів⁠, також званих заповнювачами. Мітки параметрів повинні бути прив'язані до змінних додатків за допомогою [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) перед виконанням виразу.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`query`

Текст запиту у вигляді рядка. Має складатися з одного SQL-виразу.

Вираз SQL може містити нуль або більше позначок параметрів, представлених знаками питання (`?` ) у відповідних позиціях.

> **Зауваження** :
> 
> Ці мітки можна вбудовувати лише у певні місця у виразі. Наприклад, вони дозволені у списку `VALUES()` вирази `INSERT` (щоб задати значення стовпців для рядка), або в операціях порівняння речення `WHERE` для завдання порівнюваного значення. Однак вони не дозволені як ідентифікатори (наприклад, імена таблиць або стовпців).

### Значення, що повертаються

**mysqli\_prepare()** повертає об'єкт запиту або \*\*`false`\*\*в случае ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Приклад використання** mysqli::prepare()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$city = "Amersfoort";

/* создание подготавливаемого запроса */
$stmt = $mysqli->prepare("SELECT District FROM City WHERE Name=?");

/* связывание параметров с метками */
$stmt->bind_param("s", $city);

/* выполнение запроса */
$stmt->execute();

/* связывание переменных с результатами запроса */
$stmt->bind_result($district);

/* получение значения */
$stmt->fetch();

printf("%s находится в округе %s\n", $city, $district);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$city = "Amersfoort";

/* создание подготавливаемого запроса */
$stmt = mysqli_prepare($link, "SELECT District FROM City WHERE Name=?");

/* связывание параметров с метками */
mysqli_stmt_bind_param($stmt, "s", $city);

/* выполнение запроса */
mysqli_stmt_execute($stmt);

/* связывание переменных с результатами запроса */
mysqli_stmt_bind_result($stmt, $district);

/* получение значения */
mysqli_stmt_fetch($stmt);

printf("%s находится в округе %s\n", $city, $district);
?>
```

Результат виконання наведених прикладів:

```
Amersfoort находится в округе Utrecht
```

### Дивіться також

-   [mysqli\_stmt\_execute()](mysqli-stmt.execute.md) \- Виконує підготовлене затвердження
-   [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) \- пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) \- Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt\_bind\_result()](mysqli-stmt.bind-result.md) \- Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md) \- Отримує результат із підготовленого запиту у вигляді об'єкта mysqli\_result
-   [mysqli\_stmt\_close()](mysqli-stmt.close.md) \- Закриває підготовлений запит
