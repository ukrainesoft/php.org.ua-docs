---
navigation:
  - mysqli-result.fetch-row.md: '« mysqli\_result::fetch\_row'
  - mysqli-result.field-seek.md: 'mysqli\_result::field\_seek »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::$field\_count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::$field\_count

# mysqli\_num\_fields

(PHP 5, PHP 7, PHP 8)

mysqli\_result::$field\_count -- mysqli\_num\_fields — Отримує кількість полів у наборі результатів

### Опис

Об'єктно-орієнтований стиль

int[$mysqli\_result->field\_count](mysqli-result.field-count.md)

Процедурний стиль

```methodsynopsis
mysqli_num_fields(mysqli_result $result): int
```

Повертає кількість полів у наборі результатів.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Ціле число (int), що становить кількість полів.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Name, CountryCode, District, Population FROM City ORDER BY ID LIMIT 1");

/* Получение количества полей в наборе результатов */
$field_cnt = $result->field_count;

printf("Получено %d полей.\n", $field_cnt);
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($link, "SELECT Name, CountryCode, District, Population FROM City ORDER BY ID LIMIT 1");

/* Получение количества полей в наборе результатов */
$field_cnt = mysqli_num_fields($result);

printf("Получено %d полей.\n", $field_cnt);
```

Результат виконання наведених прикладів:

```
Получено 4 полей.
```

### Дивіться також

-   [mysqli\_fetch\_field()](mysqli-result.fetch-field.md) \- Повертає наступне поле результуючого набору
