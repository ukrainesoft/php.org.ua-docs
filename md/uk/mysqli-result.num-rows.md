---
navigation:
  - mysqli-result.lengths.md: '« mysqli\_result::$lengths'
  - class.mysqli-driver.md: mysqli\_driver »
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::$num\_rows'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::$num\_rows

# mysqli\_num\_rows

(PHP 5, PHP 7, PHP 8)

mysqli\_result::$num\_rows -- mysqli\_num\_rows — Отримує кількість рядків у наборі результатів

### Опис

Об'єктно-орієнтований стиль

int|string[$mysqli\_result->num\_rows](mysqli-result.num-rows.md)

Процедурний стиль

```methodsynopsis
mysqli_num_rows(mysqli_result $result): int|string
```

Повертає число рядів у результуючій вибірці.

Поведение функции**mysqli\_num\_rows()** залежить від того, використовується буферизована або не буферизована результуюча вибірка. Функція повертає для небуферизованих наборів результатів, якщо з сервера не було отримано всі рядки.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Повертає ціле число (int), що становить кількість вибраних рядків. Повертає у небуферизованому режимі, якщо з сервера не було отримано всі рядки.

> **Зауваження** :
> 
> Якщо кількість рядків більша, ніж **`PHP_INT_MAX`**, число буде повернутий як рядок (string).

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Code, Name FROM Country ORDER BY Name");

/* Получение количества строк в наборе результатов */
$row_cnt = $result->num_rows;

printf("Получено %d строк.\n", $row_cnt);
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($link, "SELECT Code, Name FROM Country ORDER BY Name");

/* Получение количества строк в наборе результатов */
$row_cnt = mysqli_num_rows($result);

printf("Получено %d строк.\n", $row_cnt);
```

Результат виконання наведених прикладів:

```
Получено 239 строк.
```

### Примітки

> **Зауваження** :
> 
> В отличие от функции[mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.md)У цієї функції немає варіанта в об'єктно-орієнтованому стилі. В об'єктно-орієнтованому стилі використовуйте спосіб читання.

### Дивіться також

-   [mysqli\_affected\_rows()](mysqli.affected-rows.md) \- Отримує кількість рядків, порушених попередньою операцією MySQL
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
-   [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.md) \- Повертає кількість рядків, отриманих із сервера
