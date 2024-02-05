---
navigation:
  - mysqli-result.fetch-all.md: '« mysqli\_result::fetch\_all'
  - mysqli-result.fetch-assoc.md: 'mysqli\_result::fetch\_assoc »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::fetch\_array'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::fetch\_array

# mysqli\_fetch\_array

(PHP 5, PHP 7, PHP 8)

mysqli\_result::fetch\_array -- mysqli\_fetch\_array - Вибирає наступний рядок з набору результатів і поміщає її в асоціативний масив, звичайний масив або в обидва

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_array(int $mode = MYSQLI_BOTH): array|null|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_array(mysqli_result $result, int $mode = MYSQLI_BOTH): array|null|false
```

Вибирає один рядок даних із набору результатів та повертає її у вигляді масиву. Кожен наступний виклик цієї функції повертатиме наступний рядок у наборі результатів або \*\*`null`\*\*якщо рядків більше немає.

Крім зберігання даних у числових індексах масиву результатів, функція також може зберігати дані в асоціативних індексах, використовуючи імена полів набору результатів як ключі.

Якщо два і більше стовпця результату мають однакове ім'я, останній стовпець матиме пріоритет і перезапише будь-які попередні дані. У таких ситуаціях для доступу до даних всіх стовпців з однаковими іменами краще скористатися звичайними масивами, індексованими номерами стовпців.

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

`mode`

Цей необов'язковий параметр приймає значення константи, яка вказує на тип масиву, який потрібно помістити дані. Можливі значення параметра: **`MYSQLI_ASSOC`** **`MYSQLI_NUM`**или**`MYSQLI_BOTH`**

При використанні константи **`MYSQLI_ASSOC`** функція поводитиметься ідентично [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.md), а при\*\*`MYSQLI_NUM`\*\* ідентично функції [mysqli\_fetch\_row()](mysqli-result.fetch-row.md)При задании\*\*`MYSQLI_BOTH`\*\* функція створить один масив, що включає атрибути обох варіантів.

### Значення, що повертаються

Повертає масив, що представляє обраний рядок, \*\*`null`\*\*якщо в наборі результатів більше немає рядків або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysqli\_result::fetch\_array()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3";
$result = $mysqli->query($query);

/* числовой массив */
$row = $result->fetch_array(MYSQLI_NUM);
printf("%s (%s)\n", $row[0], $row[1]);

/* ассоциативный массив */
$row = $result->fetch_array(MYSQLI_ASSOC);
printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);

/* ассоциативный и числовой массивы */
$row = $result->fetch_array(MYSQLI_BOTH);
printf("%s (%s)\n", $row[0], $row["CountryCode"]);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER by ID LIMIT 3";
$result = mysqli_query($mysqli, $query);

/* числовой массив */
$row = mysqli_fetch_array($result, MYSQLI_NUM);
printf("%s (%s)\n", $row[0], $row[1]);

/* ассоциативный массив */
$row = mysqli_fetch_array($result, MYSQLI_ASSOC);
printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);

/* ассоциативный и числовой массивы */
$row = mysqli_fetch_array($result, MYSQLI_BOTH);
printf("%s (%s)\n", $row[0], $row["CountryCode"]);
```

Результат виконання наведених прикладів:

```
Kabul (AFG)
Qandahar (AFG)
Herat (AFG)
```

### Дивіться також

-   [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.md) \- Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqli\_fetch\_column()](mysqli-result.fetch-column.md) \- отримує один стовпець з наступного рядка набору результатів
-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.md) \- Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
-   [mysqli\_fetch\_object()](mysqli-result.fetch-object.md) \- Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
-   [mysqli\_data\_seek()](mysqli-result.data-seek.md) \- Переміщує покажчик результату на вибраний рядок
