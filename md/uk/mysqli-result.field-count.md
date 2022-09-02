---
navigation:
  - mysqli-result.fetch-row.md: '« mysqliresult::fetchrow'
  - mysqli-result.field-seek.md: 'mysqliresult::fieldseek »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqliresult
title: 'mysqliresult::$fieldcount'
---
# mysqliresult::$fieldcount

# mysqlinumfields

(PHP 5, PHP 7, PHP 8)

mysqliresult::$fieldcount - mysqlinumfields — Отримує кількість полів у наборі результатів

### Опис

Об'єктно-орієнтований стиль

int [$mysqliresult->fieldcount](mysqli-result.field-count.md)

Процедурний стиль

```methodsynopsis
mysqli_num_fields(mysqli_result $result): int
```

Повертає кількість полів у наборі результатів.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.md), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.md) [mysqliuseresult()](mysqli.use-result.md) або [mysqlistmtgetresult()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Ціле число (int), що становить кількість полів.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Name, CountryCode, District, Population FROM City ORDER BY ID LIMIT 1");

/* Получение количества полей в наборе результатов */
$field_cnt = $result->field_count;

printf("Получено %d полей.\n", $field_cnt);
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($link, "SELECT Name, CountryCode, District, Population FROM City ORDER BY ID LIMIT 1");

/* Получение количества полей в наборе результатов */
$field_cnt = mysqli_num_fields($result);

printf("Получено %d полей.\n", $field_cnt);
```

Результат виконання даних прикладів:

```
Получено 4 полей.
```

### Дивіться також

-   [mysqlifetchfield()](mysqli-result.fetch-field.md) - Повертає наступне поле результуючого набору
