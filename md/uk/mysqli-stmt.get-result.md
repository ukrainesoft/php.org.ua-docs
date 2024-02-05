---
navigation:
  - mysqli-stmt.free-result.md: '« mysqli\_stmt::free\_result'
  - mysqli-stmt.get-warnings.md: 'mysqli\_stmt::get\_warnings »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::get\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::get\_result

# mysqli\_stmt\_get\_result

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

mysqli\_stmt::get\_result -- mysqli\_stmt\_get\_result — Отримує результат із підготовленого запиту у вигляді об'єкта [mysqli\_result](class.mysqli-result.md)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::get_result(): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_get_result(mysqli_stmt $statement): mysqli_result|false
```

Отримує набір результатів з підготовленого запиту як об'єкта [mysqli\_result](class.mysqli-result.md). Дані будуть завантажені з сервера MySQL у PHP. Метод слід викликати лише для запитів, які виробляють набір результатів.

> **Зауваження** :
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.md)

> **Зауваження** :
> 
> Цю функцію не можна використовувати спільно з [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md). Обидві ці функції отримують повний набір результатів із сервера MySQL.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. Для успішних запитів, які виробляють набір результатів, таких як `SELECT, SHOW, DESCRIBE`или`EXPLAIN` **mysqli\_stmt\_get\_result()** поверне об'єкт [mysqli\_result](class.mysqli-result.md). Для інших успішних запитів **mysqli\_stmt\_get\_result()** поверне \*\*`false`\*\*ю[mysqli\_stmt\_errno()](mysqli-stmt.errno.md) можна використовувати, щоб розрізняти дві причини появи **`false`**; через помилку до PHP 7.4.13 для цієї мети доводилося використовувати [mysqli\_errno()](mysqli.errno.md)

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, Population, Continent FROM Country WHERE Continent=? ORDER BY Name LIMIT 1";

$stmt = $mysqli->prepare($query);
$stmt->bind_param("s", $continent);

$continentList = array('Europe', 'Africa', 'Asia', 'North America');

foreach ($continentList as $continent) {
    $stmt->execute();
    $result = $stmt->get_result();
    while ($row = $result->fetch_array(MYSQLI_NUM)) {
        foreach ($row as $r) {
            print "$r ";
        }
        print "\n";
    }
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, Population, Continent FROM Country WHERE Continent=? ORDER BY Name LIMIT 1";

$stmt = mysqli_prepare($link, $query);
mysqli_stmt_bind_param($stmt, "s", $continent);

$continentList= array('Europe', 'Africa', 'Asia', 'North America');

foreach ($continentList as $continent) {
    mysqli_stmt_execute($stmt);
    $result = mysqli_stmt_get_result($stmt);
    while ($row = mysqli_fetch_array($result, MYSQLI_NUM)) {
        foreach ($row as $r) {
            print "$r ";
        }
        print "\n";
    }
}
```

Висновок наведених прикладів буде схожим на:

```
Albania 3401200 Europe
Algeria 31471000 Africa
Afghanistan 22720000 Asia
Anguilla 8000 North America
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_result\_metadata()](mysqli-stmt.result-metadata.md) \- Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) \- пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.md) \- Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) \- Зберігає набір результатів у внутрішньому буфері
