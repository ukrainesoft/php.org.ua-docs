---
navigation:
  - mysqli-stmt.construct.md: '« mysqli\_stmt::\_\_construct'
  - mysqli-stmt.errno.md: 'mysqli\_stmt::$errno »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::data\_seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::data\_seek

# mysqli\_stmt\_data\_seek

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::data\_seek -- mysqli\_stmt\_data\_seek — Коригує покажчик результату на довільний рядок у буферизованому результаті

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::data_seek(int $offset): void
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_data_seek(mysqli_stmt $statement, int $offset): void
```

Функція переміщує покажчик буферизованого набору результатів у довільний рядок, заданий параметром `offset`

Функція працює лише з буферизованим внутрішнім набором результатів. Функція [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) повинна бути викликана до **mysqli\_stmt\_data\_seek()**

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`offset`

Значення повинне бути в діапазоні від 0 до числа рядків мінус один (0. . [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name";
$stmt = $mysqli->prepare($query);
$stmt->execute();

$stmt->bind_result($name, $code);

$stmt->store_result();

/* переходим к строке 400 результирующей таблицы */
$stmt->data_seek(399);

$stmt->fetch();

printf("Город: %s  Код страны: %s\n", $name, $code);
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name";
$stmt = mysqli_prepare($link, $query);

mysqli_stmt_execute($stmt);

mysqli_stmt_bind_result($stmt, $name, $code);

mysqli_stmt_store_result($stmt);

/* переходим к строке 400 результирующей таблицы */
mysqli_stmt_data_seek($stmt, 399);

mysqli_stmt_fetch($stmt);

printf("Город: %s  Код страны: %s\n", $name, $code);
?>
```

Результат виконання наведених прикладів:

```
Город: Benin City  Код страны: NGA
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) \- Зберігає набір результатів у внутрішньому буфері
-   [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.md) \- Повертає кількість рядків, отриманих із сервера
-   [mysqli\_data\_seek()](mysqli-result.data-seek.md) \- Переміщує покажчик результату на вибраний рядок
