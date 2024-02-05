---
navigation:
  - mysqli-stmt.param-count.md: '« mysqli\_stmt::$param\_count'
  - mysqli-stmt.reset.md: 'mysqli\_stmt::reset »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::prepare'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::prepare

# mysqli\_stmt\_prepare

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::prepare -- mysqli\_stmt\_prepare — Підготовка затвердження SQL до виконання

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::prepare(string $query): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_prepare(mysqli_stmt $statement, string $query): bool
```

Готує затвердження до виконання. Запит повинен складатися з одного оператора SQL.

Шаблон затвердження може містити нуль або кілька знаків запитання (`?` ), позначок параметрів, також званих заповнювачами. Мітки параметрів повинні бути прив'язані до змінних додатків за допомогою [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) перед виконанням затвердження. рядків.

> **Зауваження** :
> 
> У разі, якщо довжина виразу, що передається в **mysqli\_stmt\_prepare()**, больше, чем`max_allowed_packet` сервера, коди помилки, що повертаються можуть відрізнятися в залежності від використовуваного драйвера. А це може бути або рідний MySQL-драйвер (`mysqlnd`), або клієнтська бібліотека MySQL (`libmysqlclient`). Поведінка функції буде такою:
> 
> -   `mysqlnd`на платформі Linux повертає код помилки 1153. Повідомлення про помилку означає розмір пакета перевищує`max_allowed_packet`байт.
>     
> -   `mysqlnd`на платформі Windows повертає код помилки 2006. Це повідомлення про помилку означає, що сервер недоступний.
>     
> -   `libmysqlclient`на всіх платформах повертає код помилки 2006 року. Це повідомлення про помилку означає сервер недоступний.
>     

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`query`

Текст запиту у вигляді рядка. Запит повинен складатися з одного виразу SQL.

Затвердження SQL може містити нуль або більше позначок параметрів, представлених знаками питання (`?` ) у відповідних позиціях.

> **Зауваження** :
> 
> Мітки параметрів запиту можна вбудовувати лише у певні місця у виразі. Наприклад, вони допустимі у списку `VALUES()` вирази `INSERT` (щоб задати значення стовпців для рядка), або в операціях порівняння речення `WHERE` для завдання порівнюваного значення. Однак ці позначки неприпустимі як ідентифікатори (наприклад, імена стовпців або таблиць).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Приклад використання** mysqli\_stmt::prepare()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$city = "Amersfoort";

/* Создаём подготовленное утверждение */
$stmt = $mysqli->stmt_init();
$stmt->prepare("SELECT District FROM City WHERE Name=?");

/* Связываем переменные с метками */
$stmt->bind_param("s", $city);

/* Выполняем запрос */
$stmt->execute();

/* Связываем переменные результата */
$stmt->bind_result($district);

/* Получаем значение */
$stmt->fetch();

printf("%s находится в районе %s\n", $city, $district);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$city = "Amersfoort";

/* Создаём подготовленное утверждение */
$stmt = mysqli_stmt_init($link);
mysqli_stmt_prepare($stmt, "SELECT District FROM City WHERE Name=?");

/* Связываем переменные с метками */
mysqli_stmt_bind_param($stmt, "s", $city);

/* Выполняем запрос */
mysqli_stmt_execute($stmt);

/* Связываем переменные результата */
mysqli_stmt_bind_result($stmt, $district);

/* Получаем значение */
mysqli_stmt_fetch($stmt);

printf("%s находится в районе %s\n", $city, $district);
```

Результат виконання наведених прикладів:

```
Amersfoort находится в районе Utrecht
```

### Дивіться також

-   [mysqli\_stmt\_init()](mysqli.stmt-init.md) \- Ініціалізує запит та повертає об'єкт для використання у mysqli\_stmt\_prepare
-   [mysqli\_stmt\_execute()](mysqli-stmt.execute.md) \- Виконує підготовлене затвердження
-   [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) \- пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) \- Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt\_bind\_result()](mysqli-stmt.bind-result.md) \- Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md) \- Отримує результат із підготовленого запиту у вигляді об'єкта mysqli\_result
-   [mysqli\_stmt\_close()](mysqli-stmt.close.md) \- Закриває підготовлений запит
