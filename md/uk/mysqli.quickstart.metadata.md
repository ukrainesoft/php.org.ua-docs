Метадані

-   [« API поддержка транзакций](mysqli.quickstart.transactions.html)
    
-   [Установка и настройка »](mysqli.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Краткое руководство](mysqli.quickstart.html)
    
-   Метадані
    

## Метадані

Результуючий набір MySQL містить метадані. Ці дані описують стовпці результуючої таблиці. Усі відомості, які передає MySQL, доступні через `mysqli` інтерфейс. Модуль не змінює отримані дані або ці зміни незначні. Відмінності між версіями MySQL також можна не брати до уваги.

Метадані доступні через інтерфейс [mysqliresult](class.mysqli-result.html)

**Приклад #1 Доступ до метаданих результуючої таблиці**

```php
<?php
$mysqli = new mysqli("example.com", "user", "password", "database");
if ($mysqli->connect_errno) {
    echo "Не удалось подключиться к MySQL: (" . $mysqli->connect_errno . ") " . $mysqli->connect_error;
}

$res = $mysqli->query("SELECT 1 AS _one, 'Hello' AS _two FROM DUAL");
var_dump($res->fetch_fields());
?>
```

Результат виконання цього прикладу:

```
array(2) {
  [0]=>
  object(stdClass)#3 (13) {
    ["name"]=>
    string(4) "_one"
    ["orgname"]=>
    string(0) ""
    ["table"]=>
    string(0) ""
    ["orgtable"]=>
    string(0) ""
    ["def"]=>
    string(0) ""
    ["db"]=>
    string(0) ""
    ["catalog"]=>
    string(3) "def"
    ["max_length"]=>
    int(1)
    ["length"]=>
    int(1)
    ["charsetnr"]=>
    int(63)
    ["flags"]=>
    int(32897)
    ["type"]=>
    int(8)
    ["decimals"]=>
    int(0)
  }
  [1]=>
  object(stdClass)#4 (13) {
    ["name"]=>
    string(4) "_two"
    ["orgname"]=>
    string(0) ""
    ["table"]=>
    string(0) ""
    ["orgtable"]=>
    string(0) ""
    ["def"]=>
    string(0) ""
    ["db"]=>
    string(0) ""
    ["catalog"]=>
    string(3) "def"
    ["max_length"]=>
    int(5)
    ["length"]=>
    int(5)
    ["charsetnr"]=>
    int(8)
    ["flags"]=>
    int(1)
    ["type"]=>
    int(253)
    ["decimals"]=>
    int(31)
  }
}
```

*Підготовлювані запити*

Метадані результуючих наборів, одержаних в результаті виконання підготовлених запитів, можна отримати аналогічним чином. Відповідний дескриптор [mysqliresult](class.mysqli-result.html) можна отримати функцією [mysqlistmt::resultmetadata()](mysqli-stmt.result-metadata.html)

**Приклад #2 Метадані підготовлених запитів**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$stmt = $mysqli->prepare("SELECT 1 AS _one, 'Hello' AS _two FROM DUAL");
$stmt->execute();
$result = $stmt->result_metadata();
var_dump($result->fetch_fields());
```

*Дивіться також*

-   [mysqli::query()](mysqli.query.html)
-   [mysqliresult::fetchfields()](mysqli-result.fetch-fields.html)