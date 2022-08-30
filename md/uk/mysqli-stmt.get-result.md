Отримує результат підготовленого запиту у вигляді об'єкта mysqliresult

-   [« mysqlistmt::freeresult](mysqli-stmt.free-result.html)
    
-   [mysqlistmt::getwarnings »](mysqli-stmt.get-warnings.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlistmt](class.mysqli-stmt.html)
    
-   Отримує результат підготовленого запиту у вигляді об'єкта mysqliresult
    

# mysqlistmt::getresult

# mysqlistmtgetresult

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqlistmt::getresult -- mysqlistmtgetresult — Отримує результат із підготовленого запиту у вигляді об'єкта [mysqliresult](class.mysqli-result.html)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::get_result(): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_get_result(mysqli_stmt $statement): mysqli_result|false
```

Отримує набір результатів з підготовленого запиту як об'єкта [mysqliresult](class.mysqli-result.html). Дані будуть завантажені з сервера MySQL у PHP. Метод слід викликати лише для запитів, які виробляють набір результатів.

> **Зауваження**
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.html)

> **Зауваження**
> 
> Цю функцію не можна використовувати спільно з [mysqlistmtstoreresult()](mysqli-stmt.store-result.html). Обидві ці функції отримують повний набір результатів із сервера MySQL.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. Для успішних запитів, які виробляють набір результатів, таких як `SELECT, SHOW, DESCRIBE` або `EXPLAIN` **mysqlistmtgetresult()** поверне об'єкт [mysqliresult](class.mysqli-result.html). Для інших успішних запитів **mysqlistmtgetresult()** поверне **`false`**. функцію [mysqlistmterrno()](mysqli-stmt.errno.html) можна використовувати, щоб розрізняти дві причини появи **`false`**; через помилку до PHP 7.4.13 для цієї мети доводилося використовувати [mysqlierrno()](mysqli.errno.html)

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, Population, Continent FROM Country WHERE Continent=? ORDER BY Name LIMIT 1";

$stmt = $mysqli->prepare($query);
$stmt->bind_param("s", $continent);

$continentList = array('Europe', 'Africa', 'Asia', 'North America');

foreach ($continentList as $continent) {
    $stmt->execute();
    $result = $stmt->get_result();
    while ($row = $result->fetch_array(MYSQLI_NUM)) {
        foreach ($row as $r) {
            print "$r ";
        }
        print "\n";
    }
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, Population, Continent FROM Country WHERE Continent=? ORDER BY Name LIMIT 1";

$stmt = mysqli_prepare($link, $query);
mysqli_stmt_bind_param($stmt, "s", $continent);

$continentList= array('Europe', 'Africa', 'Asia', 'North America');

foreach ($continentList as $continent) {
    mysqli_stmt_execute($stmt);
    $result = mysqli_stmt_get_result($stmt);
    while ($row = mysqli_fetch_array($result, MYSQLI_NUM)) {
        foreach ($row as $r) {
            print "$r ";
        }
        print "\n";
    }
}
```

Результатом виконання даних прикладів буде щось подібне:

```
Albania 3401200 Europe
Algeria 31471000 Africa
Afghanistan 22720000 Asia
Anguilla 8000 North America
```

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqlistmtresultmetadata()](mysqli-stmt.result-metadata.html) - Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqlistmtfetch()](mysqli-stmt.fetch.html) - пов'язує результати підготовленого виразу зі змінними
-   [mysqlifetcharray()](mysqli-result.fetch-array.html) - Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqlistmtstoreresult()](mysqli-stmt.store-result.html) - Зберігає набір результатів у внутрішньому буфері