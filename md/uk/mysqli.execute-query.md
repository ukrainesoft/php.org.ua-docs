---
navigation:
  - mysqli.error.md: '« mysqli::$error'
  - mysqli.field-count.md: 'mysqli::$field\_count »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::execute\_query'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::execute\_query

# mysqli\_execute\_query

(PHP 8 >= 8.2.0)

mysqli::execute\_query -- mysqli\_execute\_query — Підготовка, зв'язування параметрів та виконання SQL-запиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::execute_query(string $query, ?array $params = null): mysqli_result|bool
```

Процедурний стиль

```methodsynopsis
mysqli_execute_query(mysqli $mysql, string $query, ?array $params = null): mysqli_result|bool
```

Підготовляє SQL-запит, пов'язує параметри та виконує його. Метод **mysqli::execute\_query()** є скороченням для [mysqli::prepare()](mysqli.prepare.md) [mysqli\_stmt::bind\_param()](mysqli-stmt.bind-param.md) [mysqli\_stmt::execute()](mysqli-stmt.execute.md) і [mysqli\_stmt::get\_result()](mysqli-stmt.get-result.md)

Шаблон запиту може мати нуль або більше маркерів параметрів зі знаком питання (`?` ), які також називаються заповнювачами. Значення параметрів мають бути представлені у вигляді масиву (array), переданого у параметр `params`

Підготовлений запит створюється під капотом, але він ніколи не виводиться за межі функції. Неможливо отримати доступ до властивостей запиту, як це можна зробити з об'єктом [mysqli\_stmt](class.mysqli-stmt.md). Через це обмеження інформація про стан копіюється в об'єкт [mysqli](class.mysqli.md)и доступна с помощью его методов, наПриклад,[mysqli\_affected\_rows()](mysqli.affected-rows.md) або [mysqli\_error()](mysqli.error.md)

> **Зауваження** :
> 
> В случае, когда функции**mysqli\_execute\_query()** передається запит, довжина якого перевищує `max_allowed_packet` сервера, коди помилок, що повертаються, різняться в залежності від операційної системи. Поведінка така:
> 
> -   У Linux повертається код помилки 1153. Повідомлення про помилку означає, що отримано пакет розміром більше`max_allowed_packet`(got a packet bigger than`max_allowed_packet`bytes).
>     
> -   Windows повертається код помилки 2006. Повідомлення про помилку означає, що сервер недоступний (server has gone away).
>     

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`query`

Запит у вигляді рядка. Він повинен складатися з одного SQL-запиту.

SQL-запит може містити нуль або більше маркерів параметрів, представлених символами знака питання (`?` ) у відповідних позиціях.

> **Зауваження** :
> 
> Ці мітки можна вбудовувати лише у певні місця у виразі. Наприклад, вони дозволені у списку `VALUES()` вирази `INSERT` (щоб задати значення стовпців для рядка), або в операціях порівняння речення `WHERE` для завдання порівнюваного значення. Однак вони не дозволені як ідентифікатори (наприклад, імена таблиць або стовпців).

`params`

Необов'язковий список у вигляді масиву (array) з такою кількістю елементів, скільки пов'язаних параметрів у SQL-запиті. Кожне значення сприймається як рядок (string).

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. Для успішних запитів, що створюють набір результатів, таких як `SELECT, SHOW, DESCRIBE`или`EXPLAIN`, повертає об'єкт [mysqli\_result](class.mysqli-result.md). Для інших успішних запитів повертається **`true`**

### Приклади

**Приклад #1 Приклад використання** mysqli::execute\_query()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');

$query = 'SELECT Name, District FROM City WHERE CountryCode=? ORDER BY Name LIMIT 5';
$result = $mysqli->execute_query($query, ['DEU']);
foreach ($result as $row) {
    printf("%s (%s)\n", $row["Name"], $row["District"]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = 'SELECT Name, District FROM City WHERE CountryCode=? ORDER BY Name LIMIT 5';
$result = mysqli_execute_query($link, $query, ['DEU']);
foreach ($result as $row) {
    printf("%s (%s)\n", $row["Name"], $row["District"]);
}
```

Висновок наведених прикладів буде схожим на:

```
Aachen (Nordrhein-Westfalen)
Augsburg (Baijeri)
Bergisch Gladbach (Nordrhein-Westfalen)
Berlin (Berliini)
Bielefeld (Nordrhein-Westfalen)
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_execute()](mysqli-stmt.execute.md) \- Виконує підготовлене затвердження
-   [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) \- Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md) \- Отримує результат із підготовленого запиту у вигляді об'єкта mysqli\_result
