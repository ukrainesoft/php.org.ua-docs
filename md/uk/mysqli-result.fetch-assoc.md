---
navigation:
  - mysqli-result.fetch-array.md: '« mysqli\_result::fetch\_array'
  - mysqli-result.fetch-column.md: 'mysqli\_result::fetch\_column »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::fetch\_assoc'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::fetch\_assoc

# mysqli\_fetch\_assoc

(PHP 5, PHP 7, PHP 8)

mysqli\_result::fetch\_assoc -- mysqli\_fetch\_assoc - Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_assoc(): array|null|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_assoc(mysqli_result $result): array|null|false
```

Вибирає один рядок даних із набору результатів та повертає її у вигляді асоціативного масиву. Кожен наступний виклик цієї функції повертатиме наступний рядок у наборі результатів або \*\*`null`\*\*якщо рядків більше немає.

Якщо у двох і більше стовпців у наборі результатів однакове ім'я, останній стовпець матиме пріоритет і перезапише будь-які попередні дані. Для доступу до кількох стовпців з однаковим ім'ям можна використовувати функцію [mysqli\_fetch\_row()](mysqli-result.fetch-row.md) Для вибору масиву з числовим індексом або у списку вибору SQL-запиту можна використовувати псевдоніми, щоб задати стовпцям різні імена.

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Повертає асоціативний масив, що представляє обраний рядок, де кожна властивість представляє ім'я стовпця набору результатів, \*\*`null`\*\*якщо в наборі результатів більше немає рядків або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysqli\_result::fetch\_assoc()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = $mysqli->query($query);

/* извлечение ассоциативного массива */
while ($row = $result->fetch_assoc()) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = mysqli_query($mysqli, $query);

/* извлечение ассоциативного массива */
while ($row = mysqli_fetch_assoc($result)) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Висновок наведених прикладів буде схожим на:

```
Pueblo (USA)
Arvada (USA)
Cape Coral (USA)
Green Bay (USA)
Santa Clara (USA)
```

**Приклад #2 Сравнение использования[mysqli\_result](class.mysqli-result.md) [iterator](class.iterator.md)и**mysqli\_result::fetch\_assoc()\*\*\*\*

[mysqli\_result](class.mysqli-result.md) можна повторити за допомогою [foreach](control-structures.foreach.md). Результуючий набір завжди повторюватиметься з першого рядка незалежно від поточної позиції.

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = 'SELECT Name, CountryCode FROM City ORDER BY ID DESC';

// Используем итераторы
$result = $mysqli->query($query);
foreach ($result as $row) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}

echo "\n==================\n";

// Не используем итераторы
$result = $mysqli->query($query);
while ($row = $result->fetch_assoc()) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Висновок наведеного прикладу буде схожим на:

```
Pueblo (USA)
Arvada (USA)
Cape Coral (USA)
Green Bay (USA)
Santa Clara (USA)

==================
Pueblo (USA)
Arvada (USA)
Cape Coral (USA)
Green Bay (USA)
Santa Clara (USA)
```

### Дивіться також

-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.md) \- Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_fetch\_column()](mysqli-result.fetch-column.md) \- отримує один стовпець з наступного рядка набору результатів
-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.md) \- Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
-   [mysqli\_fetch\_object()](mysqli-result.fetch-object.md) \- Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
-   [mysqli\_data\_seek()](mysqli-result.data-seek.md) \- Переміщує покажчик результату на вибраний рядок
