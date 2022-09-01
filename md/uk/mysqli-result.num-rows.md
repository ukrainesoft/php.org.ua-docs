---
navigation:
  - mysqli-result.lengths.html: '« mysqliresult::$lengths'
  - class.mysqli-driver.html: mysqlidriver »
  - index.md: PHP Manual
  - class.mysqli-result.html: mysqliresult
title: 'mysqliresult::$numrows'
---
# mysqliresult::$numrows

# mysqlinumrows

(PHP 5, PHP 7, PHP 8)

mysqliresult::$numrows - mysqlinumrows — Отримує кількість рядків у наборі результатів

### Опис

Об'єктно-орієнтований стиль

int|string [$mysqliresult->numrows](mysqli-result.num-rows.html)

Процедурний стиль

```methodsynopsis
mysqli_num_rows(mysqli_result $result): int|string
```

Повертає число рядів у результуючій вибірці.

Поведінка функції **mysqlinumrows()** залежить від того, використовується буферизована або не буферизована результуюча вибірка. Функція повертає `0` для небуферизованих наборів результатів, якщо з сервера не було отримано всі рядки.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.html)

### Значення, що повертаються

Повертає ціле число (int), що становить кількість вибраних рядків. Повертає `0` у небуферизованому режимі, якщо з сервера не було отримано всі рядки.

> **Зауваження**
> 
> Якщо кількість рядків більша, ніж **`PHP_INT_MAX`**, число буде повернутий як рядок (string).

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Code, Name FROM Country ORDER BY Name");

/* Получение количества строк в наборе результатов */
$row_cnt = $result->num_rows;

printf("Получено %d строк.\n", $row_cnt);
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($link, "SELECT Code, Name FROM Country ORDER BY Name");

/* Получение количества строк в наборе результатов */
$row_cnt = mysqli_num_rows($result);

printf("Получено %d строк.\n", $row_cnt);
```

Результат виконання даних прикладів:

```
Получено 239 строк.
```

### Примітки

> **Зауваження**
> 
> На відміну від функції [mysqlistmtnumrows()](mysqli-stmt.num-rows.html)У цієї функції немає варіанта в об'єктно-орієнтованому стилі. В об'єктно-орієнтованому стилі використовуйте спосіб читання.

### Дивіться також

-   [mysqliaffectedrows()](mysqli.affected-rows.html) - Отримує кількість рядків, порушених попередньою операцією MySQL
-   [mysqlistoreresult()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання
-   [mysqliquery()](mysqli.query.md) - Виконує запит до бази даних
-   [mysqlistmtnumrows()](mysqli-stmt.num-rows.html) - Повертає кількість рядків, отриманих із сервера
