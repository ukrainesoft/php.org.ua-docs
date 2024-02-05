---
navigation:
  - mysqli.more-results.md: '« mysqli::more\_results'
  - mysqli.next-result.md: 'mysqli::next\_result »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::multi\_query'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::multi\_query

# mysqli\_multi\_query

(PHP 5, PHP 7, PHP 8)

mysqli::multi\_query -- mysqli\_multi\_query — Виконує один або кілька запитів до бази даних

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

**Увага**

# Попередження безпеки: SQL-ін'єкція

Замість складання рядку запиту з включенням змінних значень необхідно [готувати запити](mysqli.quickstart.prepared-statements.md). Або рядки запиту мають бути екрановані функцією [mysqli\_real\_escape\_string()](mysqli.real-escape-string.md) та правильно відформатовані.

Запити надсилаються асинхронно за один виклик бази даних, але база даних обробляє їх послідовно . **mysqli\_multi\_query()** очікує завершення першого запиту, перш ніж повернути керування PHP. Потім сервер MySQL обробить наступний запит у послідовності. Як тільки наступний результат буде готовий, MySQL чекатиме наступного виконання [mysqli\_next\_result()](mysqli.next-result.md)из PHP.

Для обробки кількох запитів рекомендується використовувати [do-while](control-structures.do.while.md). З'єднання буде зайнято доти, доки всі запити не будуть завершені та їх результати не будуть завантажені до PHP. Ніякий інший оператор не може бути виданий у тому ж з'єднанні, доки не будуть опрацьовані всі запити. Щоб перейти до наступного запиту у послідовності, використовуйте [mysqli\_next\_result()](mysqli.next-result.md). Якщо наступний результат ще не готовий, на mysqli буде чекати відповіді від сервера MySQL. Щоб перевірити, чи є результати, використовуйте [mysqli\_more\_results()](mysqli.more-results.md)

Для запитів, які виробляють набір результатів, таких як `SELECT, SHOW, DESCRIBE`или`EXPLAIN` [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_store\_result()](mysqli.store-result.md) може використовуватись для отримання набору результатів. Для запитів, які не роблять набір результатів, ті ж функції можуть використовуватися для отримання інформації, такої як кількість порушених рядків.

**Підказка**

Виконання запитів `CALL` для процедур, що зберігаються, може дати кілька наборів результатів. Якщо процедура, що зберігається, містить запити `SELECT`набори результатів повертаються в тому порядку, в якому вони створюються при виконанні процедури. Загалом, функція, що викликає, не може знати, скільки наборів результатів поверне процедура, і повинна бути готова отримати кілька результатів. Кінцевий результат процедури - результат статусу, який включає набір результатів. Статус показує, чи була процедура успішною чи помилка.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`query`

Рядок, що містить запити, які потрібно виконати. Декілька запитів слід розділяти крапкою з комою.

### Значення, що повертаються

Повертає \*\*`false`\*\*якщо перший вираз викликав помилку. Щоб отримати доступ до помилок інших підзапитів, потрібно спочатку викликати функцію [mysqli\_next\_result()](mysqli.next-result.md)

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Пример #1 Пример использования**mysqli::multi\_query()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполнение нескольких запросов */
$mysqli->multi_query($query);
do {
    /* сохранить набор результатов в PHP */
    if ($result = $mysqli->store_result()) {
        while ($row = $result->fetch_row()) {
            printf("%s\n", $row[0]);
        }
    }
    /* вывести разделитель */
    if ($mysqli->more_results()) {
        printf("-----------------\n");
    }
} while ($mysqli->next_result());
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполнение нескольких запросов */
mysqli_multi_query($link, $query);
do {
    /* сохранить набор результатов в PHP */
    if ($result = mysqli_store_result($link)) {
        while ($row = mysqli_fetch_row($result)) {
            printf("%s\n", $row[0]);
        }
    }
    /* вывести разделитель */
    if (mysqli_more_results($link)) {
        printf("-----------------\n");
    }
} while (mysqli_next_result($link));
```

Висновок наведених прикладів буде схожим на:

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

-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
-   [mysqli\_next\_result()](mysqli.next-result.md) \- Підготовка наступного доступного результуючого набору з multi\_query
-   [mysqli\_more\_results()](mysqli.more-results.md) \- Перевірка, чи є ще результати у мультизапиті
