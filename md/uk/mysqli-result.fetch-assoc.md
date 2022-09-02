---
navigation:
  - mysqli-result.fetch-array.md: '« mysqliresult::fetcharray'
  - mysqli-result.fetch-column.md: 'mysqliresult::fetchcolumn »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqliresult
title: 'mysqliresult::fetchassoc'
---
# mysqliresult::fetchassoc

# mysqlifetchassoc

(PHP 5, PHP 7, PHP 8)

mysqliresult::fetchassoc - mysqlifetchassoc - Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив

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

Якщо у двох і більше стовпців у наборі результатів однакове ім'я, останній стовпець матиме пріоритет і перезапише будь-які попередні дані. Для доступу до кількох стовпців з однаковим ім'ям можна використовувати функцію [mysqlifetchrow()](mysqli-result.fetch-row.md) Для вибору масиву з числовим індексом або у списку вибору SQL-запиту можна використовувати псевдоніми, щоб задати стовпцям різні імена.

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.md), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.md) [mysqliuseresult()](mysqli.use-result.md) або [mysqlistmtgetresult()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Повертає асоціативний масив, що представляє обраний рядок, де кожна властивість представляє ім'я стовпця набору результатів, \*\*`null`\*\*якщо в наборі результатів більше немає рядків або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqliresult::fetchassoc()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = $mysqli->query($query);

/* извлечение ассоциативного Масива */
while ($row = $result->fetch_assoc()) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = mysqli_query($mysqli, $query);

/* извлечение ассоциативного Масива */
while ($row = mysqli_fetch_assoc($result)) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Результатом виконання даних прикладів буде щось подібне:

```
Pueblo (USA)
Arvada (USA)
Cape Coral (USA)
Green Bay (USA)
Santa Clara (USA)
```

**Приклад #2 Порівняння використання [mysqliresult](class.mysqli-result.md) [iterator](class.iterator.md) і **mysqliresult::fetchassoc()****

[mysqliresult](class.mysqli-result.md) можна повторити за допомогою [foreach](control-structures.foreach.md). Результуючий набір завжди повторюватиметься з першого рядка незалежно від поточної позиції.

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = 'SELECT Name, CountryCode FROM City ORDER BY ID DESC';

// Используем итераторы
$result = $mysqli->query($query);
foreach ($result as $row) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}

echo "\n==================\n";

// Не используем итераторы
$result = $mysqli->query($query);
while ($row = $result->fetch_assoc()) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [mysqlifetcharray()](mysqli-result.fetch-array.md) - Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqlifetchcolumn()](mysqli-result.fetch-column.md) - отримує один стовпець з наступного рядка набору результатів
-   [mysqlifetchrow()](mysqli-result.fetch-row.md) - Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
-   [mysqlifetchobject()](mysqli-result.fetch-object.md) - Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqliquery()](mysqli.query.md) - Виконує запит до бази даних
-   [mysqlidataseek()](mysqli-result.data-seek.md) - Переміщує покажчик результату на вибраний рядок
