---
navigation:
  - mysqli-stmt.param-count.md: '« mysqlistmt::$paramcount'
  - mysqli-stmt.reset.md: 'mysqlistmt::reset »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqlistmt
title: 'mysqlistmt::prepare'
---
# mysqlistmt::prepare

# mysqlistmtprepare

(PHP 5, PHP 7, PHP 8)

mysqlistmt::prepare -- mysqlistmtprepare — Підготовка затвердження SQL до виконання

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

Шаблон затвердження може містити нуль або кілька знаків запитання (`?`), позначок параметрів⁠, також званих заповнювачами. Мітки параметрів повинні бути прив'язані до змінних додатків за допомогою [mysqlistmtbindparam()](mysqli-stmt.bind-param.md) перед виконанням затвердження. рядків.

> **Зауваження**
> 
> У випадку, якщо довжина виразу, який ви передаєте в **mysqlistmtprepare()**, більше ніж `max_allowed_packet` сервера, коди помилки, що повертаються, можуть відрізнятися в залежності від використовуваного драйвера. А це може бути або рідний MySQL-драйвер (`mysqlnd`), або клієнтська бібліотека MySQL (`libmysqlclient`). Поведінка функції буде такою:
> 
> -   `mysqlnd` на платформі Linux повертає код помилки 1153. Повідомлення про помилку означає розмір пакета перевищує `max_allowed_packet` байт.
>     
> -   `mysqlnd` на платформі Windows повертає код помилки 2006. Це повідомлення про помилку означає, що сервер недоступний.
>     
> -   `libmysqlclient` на всіх платформах повертає код помилки 2006 року. Це повідомлення про помилку означає сервер недоступний.
>     

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.md), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.md)

`query`

Текст запиту у вигляді рядка. Запит повинен складатися з одного виразу SQL.

Затвердження SQL може містити нуль або більше позначок параметрів, представлених знаками питання (`?`) у відповідних позиціях.

> **Зауваження**
> 
> Мітки параметрів запиту можна вбудовувати лише у певні місця у виразі. Наприклад, вони допустимі у списку `VALUES()` вирази `INSERT` (щоб задати значення стовпців для рядка), або в операціях порівняння речення `WHERE` для завдання порівнюваного значення.
> 
> Однак, ці мітки неприпустимі як ідентифікатори (наприклад, імена стовпців або таблиць) або завдання обох операндів бінарного оператора, такого як знак рівності `=`. Останнє обмеження необхідне, оскільки інакше неможливо визначити тип операндов. В основному параметри допустимі у виразах мови маніпулювання даними (DML), і неприпустимі у виразах мови визначення даних (DDL).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlistmt::prepare()****

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

Результат виконання даних прикладів:

```
Amersfoort находится в районе Utrecht
```

### Дивіться також

-   [mysqlistmtinit()](mysqli.stmt-init.md) - Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare
-   [mysqlistmtexecute()](mysqli-stmt.execute.md) - Виконує підготовлене затвердження
-   [mysqlistmtfetch()](mysqli-stmt.fetch.md) - пов'язує результати підготовленого виразу зі змінними
-   [mysqlistmtbindparam()](mysqli-stmt.bind-param.md) - Прив'язка змінних до параметрів запиту, що готується.
-   [mysqlistmtbindresult()](mysqli-stmt.bind-result.md) - Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqlistmtgetresult()](mysqli-stmt.get-result.md) - Отримує результат із підготовленого запиту у вигляді об'єкта mysqliresult
-   [mysqlistmtclose()](mysqli-stmt.close.md) - Закриває підготовлений запит
