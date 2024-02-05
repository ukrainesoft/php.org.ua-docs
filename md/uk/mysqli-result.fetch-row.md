---
navigation:
  - mysqli-result.fetch-object.md: '« mysqli\_result::fetch\_object'
  - mysqli-result.field-count.md: 'mysqli\_result::$field\_count »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::fetch\_row'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::fetch\_row

# mysqli\_fetch\_row

(PHP 5, PHP 7, PHP 8)

mysqli\_result::fetch\_row -- mysqli\_fetch\_row - Вибирає наступний рядок з набору результатів і поміщає його у звичайний масив

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_row(): array|null|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_row(mysqli_result $result): array|null|false
```

Вибирає один рядок даних із результуючого набору та повертає її у вигляді масиву, в якому індекси елементів відповідають номерам стовпців (починаючи з 0). Кожен наступний виклик функції повертатиме масив з даними наступного рядка набору або \*\*`null`\*\*якщо рядки закінчилися.

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Повертає нумерований масив, що представляє обраний рядок, \*\*`null`\*\*якщо в наборі результатів більше немає рядків або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysqli\_result::fetch\_row()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = $mysqli->query($query);

/* получение массива объектов */
while ($row = $result->fetch_row()) {
    printf("%s (%s)\n", $row[0], $row[1]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = mysqli_query($mysqli, $query);

/* получение ассоциативного массива */
while ($row = mysqli_fetch_row($result)) {
    printf("%s (%s)\n", $row[0], $row[1]);
}
```

Результат виконання наведених прикладів:

```
Pueblo (USA)
Arvada (USA)
Cape Coral (USA)
Green Bay (USA)
Santa Clara (USA)
```

### Дивіться також

-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.md) \- Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.md) \- Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqli\_fetch\_column()](mysqli-result.fetch-column.md) \- отримує один стовпець з наступного рядка набору результатів
-   [mysqli\_fetch\_object()](mysqli-result.fetch-object.md) \- Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
-   [mysqli\_data\_seek()](mysqli-result.data-seek.md) \- Переміщує покажчик результату на вибраний рядок
