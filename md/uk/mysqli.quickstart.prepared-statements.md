---
navigation:
  - mysqli.quickstart.statements.md: « Виконання запитів
  - mysqli.quickstart.stored-procedures.md: Збережені процедури »
  - index.md: PHP Manual
  - mysqli.quickstart.md: Короткий посібник
title: Підготовлювані запити
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Підготовлювані запити

СУБД MySQL підтримує запити, що готуються. Підготовлювані (або параметризовані) запити використовуються для підвищення ефективності, коли один запит виконується багаторазово та захищає від ін'єкцій SQL.

**Принцип роботи**

Виконання запиту, що готується, проводиться в два етапи: підготовка та виконання. На етапі підготовки на сервер надсилається шаблон запиту. Сервер виконує синтаксичну перевірку цього шаблону, будує план виконання запиту та виділяє під нього ресурси.

MySQL сервер підтримує неіменовані, або позиційні, псевдозмінні `?`

За підготовкою слідує виконання. Під час виконання клієнт пов'язує значення параметрів та відправляє їх на сервер. Сервер виконує запит із зв'язаними значеннями, використовуючи раніше створені внутрішні ресурси.

**Приклад #1 Підготовлений запит**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

/* Неподготовленный запрос */
$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label TEXT)");

/* Подготовленный запрос, шаг 1: подготовка */
$stmt = $mysqli->prepare("INSERT INTO test(id, label) VALUES (?, ?)");

/* Подготовленный запрос, шаг 2: связывание и выполнение */
$id = 1;
$label = 'PHP';
$stmt->bind_param("is", $id, $label); // "is" означает, что $id связывается, как целое число, а $label — как строка

$stmt->execute();
```

**Повторне виконання запиту**

Підготовлений запит можна запускати багаторазово. Перед кожним запуском значення прив'язаних змінних передаватимуться на сервер і підставлятимуться в текст запиту. Сам текст запиту повторно не аналізується, так само як і не надсилається повторно шаблон.

**Приклад #2 Вираз INSERT один раз готується, а потім багаторазово виконується**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

/* Неподготовленный запрос */
$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label TEXT)");

/* Подготовленный запрос, шаг 1: подготовка */
$stmt = $mysqli->prepare("INSERT INTO test(id, label) VALUES (?, ?)");

/* Подготовленный запрос, шаг 2: связывание и выполнение */
$stmt->bind_param("is", $id, $label); // "is" означает, что $id связывается, как целое число, а $label — как строка

$data = [
    1 => 'PHP',
    2 => 'Java',
    3 => 'C++'
];
foreach ($data as $id => $label) {
    $stmt->execute();
}

$result = $mysqli->query('SELECT id, label FROM test');
var_dump($result->fetch_all(MYSQLI_ASSOC));
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  array(2) {
    ["id"]=>
    string(1) "1"
    ["label"]=>
    string(3) "PHP"
  }
  [1]=>
  array(2) {
    ["id"]=>
    string(1) "2"
    ["label"]=>
    string(4) "Java"
  }
  [2]=>
  array(2) {
    ["id"]=>
    string(1) "3"
    ["label"]=>
    string(3) "C++"
  }
}
```

Кожен запит, що готується, використовує ресурси сервера. Якщо запит більше не потрібний, його необхідно одразу закрити. Якщо не зробити цього явно, запит закриється сам, але тільки коли PHP звільнить його дескриптор, як правило, це відбувається при виході запиту з області видимості або при завершенні роботи скрипта.

Використання запитів, що готуються, не завжди призводить до підвищення ефективності. Якщо параметризований запит запускається лише раз, це призводить до більшої кількості клієнт-серверних обмінів даними, ніж під час простого запиту. Саме з цієї причини у прикладі вище вираз `SELECT` виконувалося як звичайний запит.

Також є сенс розглянути SQL-синтаксис вставки безлічі значень у виразі INSERT. У прикладі вище мультивставка (значення для вставки перераховуються через кому) у пропозиції INSERT обійшлася б дешевше, ніж підготовлений запит.

**Приклад #3 Менше обміну даними під час використання мультивставок SQL**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT)");

$values = [1, 2, 3, 4];

$stmt = $mysqli->prepare("INSERT INTO test(id) VALUES (?), (?), (?), (?)");
$stmt->bind_param('iiii', ...$values);
$stmt->execute();
```

**Типи даних значень у результуючій таблиці**

У протоколі клієнт-серверної взаємодії MySQL для звичайних запитів, що готуються, визначені різні протоколи передачі даних клієнту. Параметризовані запити використовують так званий бінарний протокол. Сервер MySQL надсилає результуючий набір клієнту «як є» у двійковому форматі. Дані в таблиці не перетворюються на текст. Клієнтські бібліотеки отримують двійкові дані та намагаються перетворити значення у відповідні типи даних PHP. Наприклад, стовпець результатів запиту SQL `INT` PHP прийме і перетворює на тип integer.

**Приклад #4 Вихідні типи даних**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

/* Неподготовленный запрос */
$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label TEXT)");
$mysqli->query("INSERT INTO test(id, label) VALUES (1, 'PHP')");

$stmt = $mysqli->prepare("SELECT id, label FROM test WHERE id = 1");
$stmt->execute();
$result = $stmt->get_result();
$row = $result->fetch_assoc();

printf("id = %s (%s)\n", $row['id'], gettype($row['id']));
printf("label = %s (%s)\n", $row['label'], gettype($row['label']));
```

Результат виконання наведеного прикладу:

```
id = 1 (integer)
label = PHP (string)
```

Така поведінка не є характерною для звичайних запитів, які за умовчанням усі результати повертають у вигляді текстових рядків. Цю поведінку за умовчанням можна змінити, настроївши з'єднання відповідним чином. Після такого настроювання різниці між даними підготовлюваного та звичайного запитів вже не буде.

**Отримання результатів запиту з прив'язкою змінних**

Результати з підготовленого запиту можна отримати або прив'язавши вихідні змінні або запросивши об'єкт [mysqli\_result](class.mysqli-result.md)

Вихідні параметри слід прив'язувати після виконання запиту. Кожному стовпцю результуючої таблиці має відповідати рівно одна змінна.

**Приклад #5 Прив'язка змінних до результату запиту**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

/* Неподготовленный запрос */
$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label TEXT)");
$mysqli->query("INSERT INTO test(id, label) VALUES (1, 'PHP')");

$stmt = $mysqli->prepare("SELECT id, label FROM test WHERE id = 1");
$stmt->execute();

$stmt->bind_result($out_id, $out_label);

while ($stmt->fetch()) {
    printf("id = %s (%s), label = %s (%s)\n", $out_id, gettype($out_id), $out_label, gettype($out_label));
}
```

Результат виконання наведеного прикладу:

```
id = 1 (integer), label = PHP (string)
```

Об'єкти запитів за замовчуванням повертають небуферизовані результуючі набори. Ці таблиці ніяким чином не переносяться на клієнта, вони залишаються на сервері, займаючи його ресурси, поки клієнтський процес самостійно не витягне всі дані. Якщо клієнт не може отримати дані результуючого набору, або після закриття об'єкта запиту залишаються невибраними якісь дані, то на `mysqli` лягає відповідальність неявно підчистити це сміття за клієнтським процесом.

Також можна буферизувати дані результуючих таблиць підготовленого запиту за допомогою функції [mysqli\_stmt::store\_result()](mysqli-stmt.store-result.md)

**Вилучення результатів запиту за допомогою mysqli\_result інтерфейсу**

Замість використання прив'язки змінних до результатів запиту, результуючі таблиці можна отримувати засобами інтерфейсу mysqli\_result. Функция[mysqli\_stmt::get\_result()](mysqli-stmt.get-result.md) повертає буферизований результуючий набір рядків.

**Приклад #6 Використання mysqli\_result для вибірки результатів запиту**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

/* Неподготовленный запрос */
$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label TEXT)");
$mysqli->query("INSERT INTO test(id, label) VALUES (1, 'PHP')");

$stmt = $mysqli->prepare("SELECT id, label FROM test WHERE id = 1");
$stmt->execute();

$result = $stmt->get_result();

var_dump($result->fetch_all(MYSQLI_ASSOC));
```

Результат виконання наведеного прикладу:

```
array(1) {
  [0]=>
  array(2) {
    ["id"]=>
    int(1)
    ["label"]=>
    string(3) "PHP"
  }
}
```

Использование интерфейса[mysqli\_result](class.mysqli-result.md) має додаткову перевагу в тому, що буферизація результуючих таблиць на клієнті пропонує гнучку систему навігації по цих таблицях.

**Приклад #7 Буферизація результуючого набору для зручності читання даних**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("example.com", "user", "password", "database");

/* Неподготовленный запрос */
$mysqli->query("DROP TABLE IF EXISTS test");
$mysqli->query("CREATE TABLE test(id INT, label TEXT)");
$mysqli->query("INSERT INTO test(id, label) VALUES (1, 'PHP'), (2, 'Java'), (3, 'C++')");

$stmt = $mysqli->prepare("SELECT id, label FROM test");
$stmt->execute();

$result = $stmt->get_result();

for ($row_no = $result->num_rows - 1; $row_no >= 0; $row_no--) {
    $result->data_seek($row_no);
    var_dump($result->fetch_assoc());
}
```

Результат виконання наведеного прикладу:

```
array(2) {
  ["id"]=>
  int(3)
  ["label"]=>
  string(3) "C++"
}
array(2) {
  ["id"]=>
  int(2)
  ["label"]=>
  string(4) "Java"
}
array(2) {
  ["id"]=>
  int(1)
  ["label"]=>
  string(3) "PHP"
}
```

**Екранування та SQL-ін'єкції**

Прив'язані змінні відправляються на сервер окремо від запиту і таким чином не можуть на нього впливати. Сервер використовує ці значення безпосередньо в момент виконання вже після того, як був оброблений шаблон виразу. Прив'язані параметри не потребують екранування, тому що вони ніколи не підставляються безпосередньо в рядок запиту. Необхідно відправляти тип прив'язаної змінної на сервер, щоб визначити відповідне перетворення. Дивіться функцію [mysqli\_stmt::bind\_param()](mysqli-stmt.bind-param.md) для більшої інформації.

Такий поділ часто вважається єдиним способом убезпечитися від SQL-ін'єкції, але насправді такого ж рівня безпеки можна досягти і з непідготовленими виразами, якщо правильно відформатувати всі значення. Важливо, що правильне форматування — не те саме, що і екранування, і включає більше логіки. Таким чином, підготовлені вирази - просто більш зручний і менш схильний до помилок спосіб для досягнення такої безпеки бази даних.

**Емуляція підготовленого запиту на клієнта**

У API немає можливості емулювати підготовлювані запити на клієнта.

**Дивіться також**

-   [mysqli::\_\_construct()](mysqli.construct.md)
-   [mysqli::query()](mysqli.query.md)
-   [mysqli::prepare()](mysqli.prepare.md)
-   [mysqli\_stmt::prepare()](mysqli-stmt.prepare.md)
-   [mysqli\_stmt::execute()](mysqli-stmt.execute.md)
-   [mysqli\_stmt::bind\_param()](mysqli-stmt.bind-param.md)
-   [mysqli\_stmt::bind\_result()](mysqli-stmt.bind-result.md)
