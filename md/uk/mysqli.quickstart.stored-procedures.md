---
navigation:
  - mysqli.quickstart.prepared-statements.md: « Підготовка запитів
  - mysqli.quickstart.multiple-statement.md: Множинні запити »
  - index.md: PHP Manual
  - mysqli.quickstart.md: Краткое руководство
title: Збережені процедури
---
## Збережені процедури

СУБД MySQL підтримує процедури, що зберігаються. Під цим терміном розуміється послідовність операцій, що зберігається як єдине ціле в каталозі бази даних на сервері. Програми можуть викликати та запускати збережені процедури. Для запуску збереженої процедури використовується SQL вираз `CALL`

*Параметри*

Збережені процедури можуть мати параметри `IN` `INOUT` і `OUT` Залежно від версії MySQL. Інтерфейс mysqli не робить різниці між цими типами параметрів.

*Параметр IN*

Вхідні параметри вказуються усередині пропозиції `CALL`. При передачі вхідних параметрів важливо переконатись, що їх значення коректно екрановані.

**Приклад #1 Виклик збереженої процедури**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");

$mysqli->query("DROP PROCEDURE IF EXISTS p");
$mysqli->query("CREATE PROCEDURE p(IN id_val INT) BEGIN INSERT INTO test(id) VALUES(id_val); END;");

$mysqli->query("CALL p(1)");

$result = $mysqli->query("SELECT id FROM test");

var_dump($result->fetch_assoc());
```

Результат виконання цього прикладу:

```
array(1) {
  ["id"]=>
  string(1) "1"
}
```

*Параметр INOUT/OUT*

Значення параметрів `INOUT``OUT` доступні через змінні сесії.

**Приклад #2 Використання змінних сесії**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP PROCEDURE IF EXISTS p");
$mysqli->query('CREATE PROCEDURE p(OUT msg VARCHAR(50)) BEGIN SELECT "Hi!" INTO msg; END;');

$mysqli->query("SET @msg = ''");
$mysqli->query("CALL p(@msg)");

$result = $mysqli->query("SELECT @msg as _p_out");

$row = $result->fetch_assoc();
echo $row['_p_out'];
```

Результат виконання цього прикладу:

```
Hi!
```

Розробники додатків та фреймворків можуть надати зручніший API, в якому поряд із сесійними змінними використовується перегляд каталогів бази даних безпосередньо. Проте варто враховувати, що такий підхід знижує швидкодію.

*Обробка результуючих наборів*

Збережені процедури можуть повертати результуючі набори рядків. Таблиці результатів роботи процедури, що зберігається, не можна коректно витягти засобами [mysqli::query()](mysqli.query.md). Функція [mysqli::query()](mysqli.query.md) виконує дві операції: запускає запит і отримує перший результуючий набір, поміщаючи його в буфер. Процедури, що зберігаються, можуть повертати більше одного результуючого набору, але при використанні [mysqli::query()](mysqli.query.md) всі вони, крім першого, стануть недоступними для користувача.

Результуючі таблиці процедур, що зберігаються, витягуються функціями [mysqli::realquery()](mysqli.real-query.md) або [mysqli::multiquery()](mysqli.multi-query.md). Обидві функції дозволяють отримати будь-яку кількість результуючих наборів, повернутих SQL-запитами, таких як `CALL`. Якщо в процесі роботи не вдається отримати всі доступні результати виклику процедури, що зберігається, буде викликатися помилка.

**Приклад #3 Вилучення результатів роботи процедури, що зберігається.**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");
$mysqli->query("INSERT INTO test(id) VALUES (1), (2), (3)");

$mysqli->query("DROP PROCEDURE IF EXISTS p");
$mysqli->query('CREATE PROCEDURE p() READS SQL DATA BEGIN SELECT id FROM test; SELECT id + 1 FROM test; END;');

$mysqli->multi_query("CALL p()");

do {
    if ($result = $mysqli->store_result()) {
        printf("---\n");
        var_dump($result->fetch_all());
        $result->free();
    }
} while ($mysqli->next_result());
```

Результат виконання цього прикладу:

```
---
array(3) {
  [0]=>
  array(1) {
    [0]=>
    string(1) "1"
  }
  [1]=>
  array(1) {
    [0]=>
    string(1) "2"
  }
  [2]=>
  array(1) {
    [0]=>
    string(1) "3"
  }
}
---
array(3) {
  [0]=>
  array(1) {
    [0]=>
    string(1) "2"
  }
  [1]=>
  array(1) {
    [0]=>
    string(1) "3"
  }
  [2]=>
  array(1) {
    [0]=>
    string(1) "4"
  }
}
```

*Використання запитів, що готуються.*

Спеціальних засобів для вилучення даних при використанні запитів, що готуються, не потрібно. Інтерфейси підготовлюваних та звичайних запитів однакові. Однак, потрібно враховувати, що не всі версії MySQL підтримують підготовку в запиті SQL-виразу `CALL`

**Приклад #4 Збережені процедури та запити, що готуються.**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");
$mysqli->query("INSERT INTO test(id) VALUES (1), (2), (3)");

$mysqli->query("DROP PROCEDURE IF EXISTS p");
$mysqli->query('CREATE PROCEDURE p() READS SQL DATA BEGIN SELECT id FROM test; SELECT id + 1 FROM test; END;');

$stmt = $mysqli->prepare("CALL p()");

$stmt->execute();

do {
    if ($result = $stmt->get_result()) {
        printf("---\n");
        var_dump($result->fetch_all());
        $result->free();
    }
} while ($stmt->next_result());
```

Результат виконання цього прикладу:

```
---
array(3) {
  [0]=>
  array(1) {
    [0]=>
    int(1)
  }
  [1]=>
  array(1) {
    [0]=>
    int(2)
  }
  [2]=>
  array(1) {
    [0]=>
    int(3)
  }
}
---
array(3) {
  [0]=>
  array(1) {
    [0]=>
    int(2)
  }
  [1]=>
  array(1) {
    [0]=>
    int(3)
  }
  [2]=>
  array(1) {
    [0]=>
    int(4)
  }
}
```

Зрозуміло, підтримується прив'язка результатів до об'єкта запиту.

**Приклад #5 Збережені процедури та запити, що готуються, з використанням прив'язки результатів**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");
$mysqli->query("INSERT INTO test(id) VALUES (1), (2), (3)");

$mysqli->query("DROP PROCEDURE IF EXISTS p");
$mysqli->query('CREATE PROCEDURE p() READS SQL DATA BEGIN SELECT id FROM test; SELECT id + 1 FROM test; END;');

$stmt = $mysqli->prepare("CALL p()");

$stmt->execute();

do {
    if ($stmt->store_result()) {
        $stmt->bind_result($id_out);
        while ($stmt->fetch()) {
            echo "id = $id_out\n";
        }
    }
} while ($stmt->next_result());
```

Результат виконання цього прикладу:

```
id = 1
id = 2
id = 3
id = 2
id = 3
id = 4
```

*Дивіться також*

-   [mysqli::query()](mysqli.query.md)
-   [mysqli::multiquery()](mysqli.multi-query.md)
-   [mysqli::nextresult()](mysqli.next-result.md)
-   [mysqli::moreresults()](mysqli.more-results.md)
