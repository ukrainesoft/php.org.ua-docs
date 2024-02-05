---
navigation:
  - mysqli-stmt.sqlstate.md: '« mysqli\_stmt::$sqlstate'
  - class.mysqli-result.md: mysqli\_result »
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::store\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::store\_result

# mysqli\_stmt\_store\_result

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::store\_result -- mysqli\_stmt\_store\_result — Зберігає набір результатів у внутрішньому буфері

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::store_result(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_store_result(mysqli_stmt $statement): bool
```

Функцію слід викликати для запитів, які успішно створюють набір результатів (наприклад, `SELECT, SHOW, DESCRIBE, EXPLAIN`) тільки якщо необхідно буферизувати в PHP повний набір результатів. Кожен наступний виклик [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) повертатиме буферизовані дані.

> **Зауваження** :
> 
> В інших випадках викликати **mysqli\_stmt\_store\_result()** немає необхідності. Але якщо такий виклик здійснено, нічого страшного не станеться, це не вплине на продуктивність та цілісність даних. Щоб переконатися, що запит повернув результуючий набір, можна скористатися функцією [mysqli\_stmt\_result\_metadata()](mysqli-stmt.result-metadata.md), яка в цьому випадку поверне **`false`**

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = $mysqli->prepare($query);
$stmt->execute();

/* сохранение результата во внутреннем буфере */
$stmt->store_result();

printf("Число строк: %d.\n", $stmt->num_rows);
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = mysqli_prepare($link, $query);
mysqli_stmt_execute($stmt);

/* сохранение результата во внутреннем буфере */
mysqli_stmt_store_result($stmt);

printf("Число строк: %d.\n", mysqli_stmt_num_rows($stmt));
?>
```

Результат виконання наведених прикладів:

```
Количество строк: 20.
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_result\_metadata()](mysqli-stmt.result-metadata.md) \- Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) \- пов'язує результати підготовленого виразу зі змінними
