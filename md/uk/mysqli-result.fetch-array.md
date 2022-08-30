Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва

-   [« mysqliresult::fetchall](mysqli-result.fetch-all.html)
    
-   [mysqliresult::fetchassoc »](mysqli-result.fetch-assoc.html)
    
-   [PHP Manual](index.html)
    
-   [mysqliresult](class.mysqli-result.html)
    
-   Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
    

# mysqliresult::fetcharray

# mysqlifetcharray

(PHP 5, PHP 7, PHP 8)

mysqliresult::fetcharray - mysqlifetcharray - Вибирає наступний рядок з набору результатів і поміщає її в асоціативний масив, звичайний масив або в обидва

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

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.html) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.html)

`mode`

Цей необов'язковий параметр приймає значення константи, яка вказує на тип масиву, який потрібно помістити дані. Можливі значення параметра: **`MYSQLI_ASSOC`** **`MYSQLI_NUM`** або **`MYSQLI_BOTH`**

При використанні константи **`MYSQLI_ASSOC`** функція поводитиметься ідентично [mysqlifetchassoc()](mysqli-result.fetch-assoc.html), а при **`MYSQLI_NUM`** ідентично функції [mysqlifetchrow()](mysqli-result.fetch-row.html). При завданні **`MYSQLI_BOTH`** функція створить один масив, що включає атрибути обох варіантів.

### Значення, що повертаються

Повертає масив, що представляє обраний рядок, \*\*`null`\*\*якщо в наборі результатів більше немає рядків або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqliresult::fetcharray()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3";
$result = $mysqli->query($query);

/* числовой Масив */
$row = $result->fetch_array(MYSQLI_NUM);
printf("%s (%s)\n", $row[0], $row[1]);

/* ассоциативный Масив */
$row = $result->fetch_array(MYSQLI_ASSOC);
printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);

/* ассоциативный и числовой Масиви */
$row = $result->fetch_array(MYSQLI_BOTH);
printf("%s (%s)\n", $row[0], $row["CountryCode"]);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER by ID LIMIT 3";
$result = mysqli_query($mysqli, $query);

/* числовой Масив */
$row = mysqli_fetch_array($result, MYSQLI_NUM);
printf("%s (%s)\n", $row[0], $row[1]);

/* ассоциативный Масив */
$row = mysqli_fetch_array($result, MYSQLI_ASSOC);
printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);

/* ассоциативный и числовой Масиви */
$row = mysqli_fetch_array($result, MYSQLI_BOTH);
printf("%s (%s)\n", $row[0], $row["CountryCode"]);
```

Результат виконання даних прикладів:

```
Kabul (AFG)
Qandahar (AFG)
Herat (AFG)
```

### Дивіться також

-   [mysqlifetchassoc()](mysqli-result.fetch-assoc.html) - Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqlifetchcolumn()](mysqli-result.fetch-column.html) - отримує один стовпець з наступного рядка набору результатів
-   [mysqlifetchrow()](mysqli-result.fetch-row.html) - Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
-   [mysqlifetchobject()](mysqli-result.fetch-object.html) - Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqliquery()](mysqli.query.html) - Виконує запит до бази даних
-   [mysqlidataseek()](mysqli-result.data-seek.html) - Переміщує покажчик результату на вибраний рядок