---
navigation:
  - mysqli.quickstart.stored-procedures.html: « Збережені процедури
  - mysqli.quickstart.transactions.md: API поддержка транзакций »
  - index.md: PHP Manual
  - mysqli.quickstart.md: Краткое руководство
title: Множинні запити
---
## Множинні запити

MySQL підтримує наявність кількох SQL-запитів у тексті одного запиту, але потребує особливого звернення. Пересилання на сервер декількох виразів в одному запиті зменшує кількість клієнт-серверних взаємодій, але потребує спеціальної обробки.

Множинні запити або мультизапити повинні запускатися функцією [mysqli::multiquery()](mysqli.multi-query.html). Окремі SQL-пропозиції у мультизапиті відокремлюються крапкою з комою. Після виконання мультизапиту, всі результуючі набори, які він повернув, необхідно витягти.

MySQL-сервер підтримує наявність в одному мультизапиті підзапитів, що повертають результуючий набір, так і не повертають.

**Приклад #1 Множинні запити**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");

$sql = "SELECT COUNT(*) AS _num FROM test;
        INSERT INTO test(id) VALUES (1);
        SELECT COUNT(*) AS _num FROM test; ";

$mysqli->multi_query($sql);

do {
    if ($result = $mysqli->store_result()) {
        var_dump($result->fetch_all(MYSQLI_ASSOC));
        $result->free();
    }
} while ($mysqli->next_result());
```

Результат виконання цього прикладу:

```
array(1) {
  [0]=>
  array(1) {
    ["_num"]=>
    string(1) "0"
  }
}
array(1) {
  [0]=>
  array(1) {
    ["_num"]=>
    string(1) "1"
  }
}
```

*Розгляд аспектів безпеки*

Функції API [mysqli::query()](mysqli.query.md) і [mysqli::realquery()](mysqli.real-query.html) під час роботи не встановлюють на сервері спеціальний прапор, необхідний виконання мультизапросов. Окрема функція API для мультизапитів дозволяє знизити ймовірність випадкових SQL-ін'єкцій. Зловмисник може спробувати додати до кінця запиту виразу, на кшталт `; DROP DATABASE mysql` або `; SELECT SLEEP(999)`. Якщо йому це вдасться, але не використовуватиметься функція `mysqli::multi_query`, сервер не виконає впроваджений та небезпечний SQL-вираз.

**Приклад #2 SQL-ін'єкція**

```php
<?php
$mysqli = new mysqli("example.com", "user", "password", "database");
$result = $mysqli->query("SELECT 1; DROP TABLE mysql.user");
if (!$result) {
    echo "Ошибка во время выполнения запроса: (" . $mysqli->errno . ") " . $mysqli->error;
}
?>
```

Результат виконання цього прикладу:

```
Ошибка во время выполнения запроса: (1064) You have an error in your SQL syntax;
check the manual that corresponds to your MySQL server version for the right syntax
to use near 'DROP TABLE mysql.user' at line 1
```

*Підготовлювані запити*

Використання безлічі виразів у запиті, що готується, не підтримується.

*Дивіться також*

-   [mysqli::query()](mysqli.query.md)
-   [mysqli::multiquery()](mysqli.multi-query.html)
-   [mysqli::nextresult()](mysqli.next-result.html)
-   [mysqli::moreresults()](mysqli.more-results.html)
