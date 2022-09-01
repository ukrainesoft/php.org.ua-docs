---
navigation:
  - mysqli-stmt.sqlstate.html: '« mysqlistmt::$sqlstate'
  - class.mysqli-result.html: mysqliresult »
  - index.html: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::storeresult'
---
# mysqlistmt::storeresult

# mysqlistmtstoreresult

(PHP 5, PHP 7, PHP 8)

mysqlistmt::storeresult -- mysqlistmtstoreresult — Зберігає набір результатів у внутрішньому буфері

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::store_result(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_store_result(mysqli_stmt $statement): bool
```

Функцію слід викликати для запитів, які успішно створюють набір результатів (наприклад, `SELECT, SHOW, DESCRIBE, EXPLAIN`) тільки якщо необхідно буферизувати в PHP повний набір результатів. Кожен наступний виклик [mysqlistmtfetch()](mysqli-stmt.fetch.html) повертатиме буферизовані дані.

> **Зауваження**
> 
> В інших випадках викликати **mysqlistmtstoreresult()** немає необхідності. Але якщо такий виклик здійснено, нічого страшного не станеться, це не вплине на продуктивність та цілісність даних. Щоб переконатися, що запит повернув результуючий набір, можна скористатися функцією [mysqlistmtresultmetadata()](mysqli-stmt.result-metadata.html), яка в цьому випадку поверне **`false`**

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = $mysqli->prepare($query);
$stmt->execute();

/* сохранение результата во внутреннем буфере */
$stmt->store_result();

printf("Число строк: %d.\n", $stmt->num_rows);
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = mysqli_prepare($link, $query);
mysqli_stmt_execute($stmt);

/* сохранение результата во внутреннем буфере */
mysqli_stmt_store_result($stmt);

printf("Число строк: %d.\n", mysqli_stmt_num_rows($stmt));
?>
```

Результат виконання даних прикладів:

```
Количество строк: 20.
```

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqlistmtresultmetadata()](mysqli-stmt.result-metadata.html) - Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqlistmtfetch()](mysqli-stmt.fetch.html) - пов'язує результати підготовленого виразу зі змінними
