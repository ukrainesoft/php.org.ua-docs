---
navigation:
  - mysqli-result.data-seek.md: '« mysqli\_result::data\_seek'
  - mysqli-result.fetch-array.md: 'mysqli\_result::fetch\_array »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::fetch\_all'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::fetch\_all

# mysqli\_fetch\_all

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

mysqli\_result::fetch\_all -- mysqli\_fetch\_all - Вибирає всі рядки з результуючого набору і поміщає їх в асоціативний масив, звичайний масив або в обидва

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

> **Зауваження** :
> 
> До PHP 8.1.0, функція доступна лише з [mysqlnd](book.mysqlnd.md)

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

`mode`

Цей необов'язковий параметр приймає значення константи, яка вказує на тип масиву, який потрібно помістити дані. Можливі значення параметра: **`MYSQLI_ASSOC`** **`MYSQLI_NUM`**или**`MYSQLI_BOTH`**

### Значення, що повертаються

Повертає масив, що містить асоціативні або звичайні масиви з даними результуючої таблиці.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Тепер також доступно при збиранні з libmysqlclient. |

### Приклади

**Пример #1 Пример использования**mysqli\_result::fetch\_all()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

$rows = $result->fetch_all(MYSQLI_ASSOC);
foreach ($rows as $row) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($mysqli, "SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

$rows = mysqli_fetch_all($result, MYSQLI_ASSOC);
foreach ($rows as $row) {
    printf("%s (%s)\n", $row["Name"], $row["CountryCode"]);
}
```

Результат виконання наведених прикладів:

```
Kabul (AFG)
Qandahar (AFG)
Herat (AFG)
```

### Дивіться також

-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.md) \- Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_fetch\_column()](mysqli-result.fetch-column.md) \- отримує один стовпець з наступного рядка набору результатів
-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
