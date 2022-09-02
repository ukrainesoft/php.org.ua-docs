---
navigation:
  - mysqli.more-results.md: '« mysqli::moreresults'
  - mysqli.next-result.md: 'mysqli::nextresult »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::multiquery'
---
# mysqli::multiquery

# mysqlimultiquery

(PHP 5, PHP 7, PHP 8)

mysqli::multiquery -- mysqlimultiquery — Виконує один або кілька запитів до бази даних

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::multi_query(string $query): bool
```

Процедурний стиль

```methodsynopsis
mysqli_multi_query(mysqli $mysql, string $query): bool
```

Запускає один або кілька запитів, перерахованих через точку з комою.

Запити надсилаються асинхронно за один виклик бази даних, але база даних обробляє їх послідовно . **mysqlimultiquery()** очікує завершення першого запиту, перш ніж повернути керування PHP. Потім сервер MySQL обробить наступний запит у послідовності. Як тільки наступний результат буде готовий, MySQL чекатиме наступного виконання [mysqlinextresult()](mysqli.next-result.md) з PHP.

Для обробки кількох запитів рекомендується використовувати [do-while](control-structures.do.while.md). З'єднання буде зайнято доти, доки всі запити не будуть завершені та їх результати не будуть завантажені до PHP. Ніякий інший оператор не може бути виданий у тому ж з'єднанні, доки не будуть опрацьовані всі запити. Щоб перейти до наступного запиту у послідовності, використовуйте [mysqlinextresult()](mysqli.next-result.md). Якщо наступний результат ще не готовий, на mysqli буде чекати відповіді від сервера MySQL. Щоб перевірити, чи є результати, використовуйте [mysqlimoreresults()](mysqli.more-results.md)

Для запитів, які виробляють набір результатів, таких як `SELECT, SHOW, DESCRIBE` або `EXPLAIN` [mysqliuseresult()](mysqli.use-result.md) або [mysqlistoreresult()](mysqli.store-result.md) може використовуватись для отримання набору результатів. Для запитів, які не здійснюють набір результатів, ті ж функції можуть використовуватися для отримання інформації, такої як кількість порушених рядків.

**Підказка**

Виконання запитів `CALL` для збережених процедур може дати кілька наборів результатів. Якщо процедура, що зберігається, містить запити `SELECT`набори результатів повертаються в тому порядку, в якому вони створюються при виконанні процедури. Загалом, функція, що викликає, не може знати, скільки наборів результатів поверне процедура, і повинна бути готова отримати кілька результатів. Кінцевий результат процедури - результат статусу, який включає набір результатів. Статус показує, чи була процедура успішною чи помилка.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

`query`

Рядок, що містить запити, які потрібно виконати. Декілька запитів слід розділяти крапкою з комою.

**Увага**

# Попередження безпеки: SQL-ін'єкція

Якщо запит містить будь-які вхідні змінні, натомість слід використовувати [запити, що готуються](mysqli.quickstart.prepared-statements.md). Як альтернатива дані повинні бути правильно відформатовані і всі рядки повинні бути екрановані за допомогою функції [mysqlirealescapestring()](mysqli.real-escape-string.md)

### Значення, що повертаються

Повертає \*\*`false`\*\*якщо перший вираз викликав помилку. Щоб отримати доступ до помилок інших підзапитів, потрібно спочатку викликати функцію [mysqlinextresult()](mysqli.next-result.md)

### Приклади

**Приклад #1 Приклад використання **mysqli::multiquery()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполнение нескольких запросов */
$mysqli->multi_query($query);
do {
    /* сохранить набор результатов в PHP */
    if ($result = $mysqli->store_result()) {
        while ($row = $result->fetch_row()) {
            printf("%s\n", $row[0]);
        }
    }
    /* вывести разделитель */
    if ($mysqli->more_results()) {
        printf("-----------------\n");
    }
} while ($mysqli->next_result());
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполнение нескольких запросов */
mysqli_multi_query($link, $query);
do {
    /* сохранить набор результатов в PHP */
    if ($result = mysqli_store_result($link)) {
        while ($row = mysqli_fetch_row($result)) {
            printf("%s\n", $row[0]);
        }
    }
    /* вывести разделитель */
    if (mysqli_more_results($link)) {
        printf("-----------------\n");
    }
} while (mysqli_next_result($link));
```

Результатом виконання даних прикладів буде щось подібне:

```
my_user@localhost
-----------------
Amersfoort
Maastricht
Dordrecht
Leiden
Haarlemmermeer
```

### Дивіться також

-   [mysqliquery()](mysqli.query.md) - Виконує запит до бази даних
-   [mysqliuseresult()](mysqli.use-result.md) - Готує результуючий набір на сервері для використання
-   [mysqlistoreresult()](mysqli.store-result.md) - передає на клієнта результуючий набір останнього запиту
-   [mysqlinextresult()](mysqli.next-result.md) - Підготовка наступного доступного результуючого набору з multiquery
-   [mysqlimoreresults()](mysqli.more-results.md) - Перевірка, чи є ще результати у мультизапиті
