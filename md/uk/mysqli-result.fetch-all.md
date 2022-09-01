---
navigation:
  - mysqli-result.data-seek.html: '« mysqliresult::dataseek'
  - mysqli-result.fetch-array.html: 'mysqliresult::fetcharray »'
  - index.md: PHP Manual
  - class.mysqli-result.html: mysqliresult
title: 'mysqliresult::fetchall'
---
# mysqliresult::fetchall

# mysqlifetchall

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqliresult::fetchall - mysqlifetchall - Вибирає всі рядки з результуючого набору і поміщає їх в асоціативний масив, звичайний масив або в обидва

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_all(int $mode = MYSQLI_NUM): array
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_all(mysqli_result $result, int $mode = MYSQLI_NUM): array
```

Повертає двовимірний масив всіх рядків результатів у вигляді асоціативного масиву, числового масиву або обох.

> **Зауваження**
> 
> До PHP 8.1.0, функція доступна лише з [mysqlnd](book.mysqlnd.md)

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.html)

`mode`

Цей необов'язковий параметр приймає значення константи, яка вказує на тип масиву, який потрібно помістити дані. Можливі значення параметра: **`MYSQLI_ASSOC`** **`MYSQLI_NUM`** або **`MYSQLI_BOTH`**

### Значення, що повертаються

Повертає масив, що містить асоціативні або звичайні масиви з даними результуючої таблиці.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер також доступно при збиранні з libmysqlclient. |

### Приклади

**Приклад #1 Приклад використання **mysqliresult::fetchall()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

$rows = $result->fetch_all(MYSQLI_ASSOC);
foreach ($rows as $row) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($mysqli, "SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

$rows = mysqli_fetch_all($result, MYSQLI_ASSOC);
foreach ($rows as $row) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Результат виконання даних прикладів:

```
Kabul (AFG)
Qandahar (AFG)
Herat (AFG)
```

### Дивіться також

-   [mysqlifetcharray()](mysqli-result.fetch-array.html) - Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqlifetchcolumn()](mysqli-result.fetch-column.html) - отримує один стовпець з наступного рядка набору результатів
-   [mysqliquery()](mysqli.query.md) - Виконує запит до бази даних
