---
navigation:
  - mysqli.prepare.md: '« mysqli::prepare'
  - mysqli.real-connect.md: 'mysqli::real\_connect »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::query'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::query

# mysqli\_query

(PHP 5, PHP 7, PHP 8)

mysqli::query -- mysqli\_query — Виконує запит до бази даних

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::query(string $query, int $result_mode = MYSQLI_STORE_RESULT): mysqli_result|bool
```

Процедурний стиль

```methodsynopsis
mysqli_query(mysqli $mysql, string $query, int $result_mode = MYSQLI_STORE_RESULT): mysqli_result|bool
```

Виконує запит `query` до бази даних.

**Увага**

# Попередження безпеки: SQL-ін'єкція

Замість складання рядку запиту з включенням змінних значень необхідно [готувати запити](mysqli.quickstart.prepared-statements.md). Або рядки запиту мають бути екрановані функцією [mysqli\_real\_escape\_string()](mysqli.real-escape-string.md) та правильно відформатовані.

Для не DML-запитів (не INSERT, UPDATE чи DELETE), ця функція рівносильна виклику функції [mysqli\_real\_query()](mysqli.real-query.md), а затем[mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_store\_result()](mysqli.store-result.md)

> **Зауваження** :
> 
> Якщо довжина передається в функцію **mysqli\_query()** вирази більше значення системної змінної `max_allowed_packet`сервера, будет сгенерирована ошибка. MySQL-драйвер (`mysqlnd`) та клієнтська бібліотека MySQL (`libmysqlclient`) викидають різні коди помилок. Поведінка функції буде такою:
> 
> -   `mysqlnd`на платформі Linux повертає код помилки 1153. Повідомлення про помилку означає розмір пакета перевищує`max_allowed_packet`байт.
>     
> -   `mysqlnd`на платформі Windows повертає код помилки 2006 року. Це повідомлення про помилку означає відмову сервера.
>     
> -   `libmysqlclient`на всіх платформах повертає код помилки 2006 року. Це повідомлення про помилку означає відмову сервера.
>     

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`query`

Текст запиту.

`result_mode`

Режим результату може бути однією з трьох констант, які вказують, як результат буде повернено сервером MySQL.

**`MYSQLI_STORE_RESULT`** (за замовчуванням) – повертає об'єкт [mysqli\_result](class.mysqli-result.md) із буферизованим набором результатів.

**`MYSQLI_USE_RESULT`** - Повертає об'єкт [mysqli\_result](class.mysqli-result.md) із небуферизованим набором результатів. Поки є відкладені записи, що очікують вибірки, лінія з'єднання буде зайнята і всі наступні дзвінки повертатимуть помилку `Commands out of sync`. Щоб уникнути помилки, всі записи повинні бути отримані з сервера або набір результатів має бути відкинуто шляхом виклику [mysqli\_free\_result()](mysqli-result.free.md)

**`MYSQLI_ASYNC`** (Доступно з mysqlnd) - запит виконується асинхронно, набір результатів відразу не повертається. Потім викликають функцію [mysqli\_poll()](mysqli.poll.md) для отримання результатів за цими запитами. Можна використовувати у поєднанні з константою **`MYSQLI_STORE_RESULT`** або **`MYSQLI_USE_RESULT`**

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. У разі успішного виконання запитів, які створюють набір результатів, таких як `SELECT, SHOW, DESCRIBE`или`EXPLAIN`, функция**mysqli\_query()** поверне об'єкт [mysqli\_result](class.mysqli-result.md). Для решти успішних запитів **mysqli\_query()** поверне **`true`**

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Приклад використання** mysqli::query()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Создание таблицы, не возвращает набор результатов */
$mysqli->query("CREATE TEMPORARY TABLE myCity LIKE City");
printf("Таблица myCity создана.\n");

/* Запросы SELECT, возвращают набор результатов */
$result = $mysqli->query("SELECT Name FROM City LIMIT 10");
printf("Запрос SELECT вернул %d строк.\n", $result->num_rows);

/* Если нужно извлечь большой объем данных, используем MYSQLI_USE_RESULT */
$result = $mysqli->query("SELECT * FROM City", MYSQLI_USE_RESULT);

/* Важно заметить, что мы не можем вызывать функции, которые взаимодействуют
   с сервером, пока не закроем набор результатов. Все подобные вызовы
   будут вызывать ошибку 'out of sync' */
$mysqli->query("SET @a:='this will not work'");
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Создание таблицы, не возвращает набор результатов */
mysqli_query($link, "CREATE TEMPORARY TABLE myCity LIKE City");
printf("Таблица myCity создана.\n");

/* Запросы SELECT, возвращают набор результатов */
$result = mysqli_query($link, "SELECT Name FROM City LIMIT 10");
printf("Запрос SELECT вернул %d строк.\n", mysqli_num_rows($result));

/* Если нужно извлечь большой объем данных, используем MYSQLI_USE_RESULT */
$result = mysqli_query($link, "SELECT * FROM City", MYSQLI_USE_RESULT);

/* Важно заметить, что мы не можем вызывать функции, которые взаимодействуют
   с сервером, пока не закроем набор результатов. Все подобные вызовы
   будут вызывать ошибку 'out of sync' */
mysqli_query($link, "SET @a:='this will not work'");
```

Результат виконання наведених прикладів:

```
Таблица myCity создана.
Запрос SELECT вернул 10 строк.

Fatal error: Uncaught mysqli_sql_exception: Commands out of sync; you can't run this command now in...
```

### Дивіться також

-   [mysqli\_execute\_query()](mysqli.execute-query.md) \- готує, зв'язує параметри та виконує SQL-запит
-   [mysqli\_real\_query()](mysqli.real-query.md) \- Виконання SQL запиту
-   [mysqli\_multi\_query()](mysqli.multi-query.md) \- Виконує один або кілька запитів до бази даних
-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_free\_result()](mysqli-result.free.md) \- звільняє пам'ять, зайняту результатами запиту
