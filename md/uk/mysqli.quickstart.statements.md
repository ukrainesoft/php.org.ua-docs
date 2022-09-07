---
navigation:
  - mysqli.quickstart.connections.md: « Соединения
  - mysqli.quickstart.prepared-statements.md: Підготовлювані запити »
  - index.md: PHP Manual
  - mysqli.quickstart.md: Краткое руководство
title: Виконання запитів
---
## Виконання запитів

За виконання запитів відповідають функції [mysqli::query()](mysqli.query.md) [mysqli::realquery()](mysqli.real-query.md) і [mysqli::multiquery()](mysqli.multi-query.md). Найчастіше застосовується функція [mysqli::query()](mysqli.query.md)оскільки вона виконує відразу дві задачі: виконує запит і буферизує на клієнті результат цього запиту (якщо він є). Виклик [mysqli::query()](mysqli.query.md) ідентичний послідовному виклику функцій [mysqli::realquery()](mysqli.real-query.md) і [mysqli::storeresult()](mysqli.store-result.md)

**Приклад #1 Виконання запитів**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");
```

*Буферизація результатів запиту*

Після виконання запиту результати можна отримати відразу, або вважати рядок за рядком з сервера. Буферизація набору результатів за клієнта дозволяє серверу якомога раніше звільнити ресурси, пов'язані з результатами запиту. Простіше кажучи, покупці повільно використовують набори результатів. Тому рекомендується використовувати буферизовані набори результатів . [mysqli::query()](mysqli.query.md) поєднує виконання запиту та буферизацію набору результатів.

PHP-програми можуть вільно оперувати даними всередині буферизованих результуючих наборів. Швидка навігація рядками наборів обумовлена ​​тим, що набори повністю розташовуються в пам'яті клієнта. Слід пам'ятати, що найчастіше обробка результатів клієнта простіше, ніж засобами сервера.

**Приклад #2 Навігація рядками буферизованої результуючої таблиці**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");
$mysqli->query("INSERT INTO test(id) VALUES (1), (2), (3)");

$result = $mysqli->query("SELECT id FROM test ORDER BY id ASC");

echo "Обратный порядок...\n";
for ($row_no = $result->num_rows - 1; $row_no >= 0; $row_no--) {
    $result->data_seek($row_no);
    $row = $result->fetch_assoc();
    echo " id = " . $row['id'] . "\n";
}

echo "Исходный порядок строк...\n";
foreach ($result as $row) {
    echo " id = " . $row['id'] . "\n";
}
```

Результат виконання цього прикладу:

```
Обратный порядок...
 id = 3
 id = 2
 id = 1
Исходный порядок строк...
 id = 1
 id = 2
 id = 3
```

*Небуферизовані результуючі набори*

Якщо клієнтські ресурси обмежені, і в той же час не потрібно підтримувати низьке навантаження на сервер, можна використовувати буферизовані результуючі набори. Навігація за такими таблицями неможлива, тому що так чи інакше мають бути оброблені всі рядки набору.

**Приклад #3 Навігація рядками небуферизованої результуючої таблиці**

```php
<?php
$mysqli->real_query("SELECT id FROM test ORDER BY id ASC");
$result = $mysqli->use_result();

echo "Порядок строк в результирующем наборе...\n";
foreach ($result as $row) {
    echo " id = " . $row['id'] . "\n";
}
```

*Типи даних значень у результуючій таблиці*

Функції [mysqli::query()](mysqli.query.md) [mysqli::realquery()](mysqli.real-query.md) і [mysqli::multiquery()](mysqli.multi-query.md) призначені для виконання запитів, що не готуються. На рівні протоколу клієнт-серверної взаємодії MySQL за виконання запитів відповідає команда `COM_QUERY` та текстовий протокол. Коли використовується текстовий протокол, сервер MySQL перед відправкою клієнту перетворює всі дані в результуючому наборі текстових рядків. Це перетворення виконується незалежно від типу даних SQL-стовпця результуючої таблиці. Клієнтські бібліотеки mysql, своєю чергою, отримують усі дані, приймаючи їх за рядки. На клієнті не проводиться жодного зворотного перетворення до вихідних типів, всі дані, отримані програмою залишаються PHP рядками.

**Приклад #4 Текстовий протокол за промовчанням повертає рядки**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label CHAR(1))");
$mysqli->query("INSERT INTO test(id, label) VALUES (1, 'a')");

$result = $mysqli->query("SELECT id, label FROM test WHERE id = 1");
$row = $result->fetch_assoc();

printf("id = %s (%s)\n", $row['id'], gettype($row['id']));
printf("label = %s (%s)\n", $row['label'], gettype($row['label']));
```

Результат виконання цього прикладу:

```
id = 1 (string)
label = a (string)
```

Якщо використовується бібліотека mysqlnd, можна включити перетворення цілих чисел і чисел з плаваючою точкою зі стовпців таблиці в PHP числа. Робиться це завданням налаштування підключення **`MYSQLI_OPT_INT_AND_FLOAT_NATIVE`**. У такому випадку mysqlnd перевірятиме метадані стовпців і перетворюватиме SQL-числа цих полів на PHP-числа, якщо ці значення не виходять за рамки допустимих діапазонів типів даних PHP. Тобто, наприклад, SQL INT число потрапить до PHP додатку у вигляді цілого (integer).

**Приклад #5 Отримання вихідних типів даних у програмі**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);

$mysqli = new mysqli();
$mysqli->options(MYSQLI_OPT_INT_AND_FLOAT_NATIVE, 1);
$mysqli->real_connect("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label CHAR(1))");
$mysqli->query("INSERT INTO test(id, label) VALUES (1, 'a')");

$result = $mysqli->query("SELECT id, label FROM test WHERE id = 1");
$row = $result->fetch_assoc();

printf("id = %s (%s)\n", $row['id'], gettype($row['id']));
printf("label = %s (%s)\n", $row['label'], gettype($row['label']));
```

Результат виконання цього прикладу:

```
id = 1 (integer)
label = a (string)
```

*Дивіться також*

-   [mysqli::construct()](mysqli.construct.md)
-   [mysqli::options()](mysqli.options.md)
-   [mysqli::realconnect()](mysqli.real-connect.md)
-   [mysqli::query()](mysqli.query.md)
-   [mysqli::multiquery()](mysqli.multi-query.md)
-   [mysqli::useresult()](mysqli.use-result.md)
-   [mysqli::storeresult()](mysqli.store-result.md)
