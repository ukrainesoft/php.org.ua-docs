---
navigation:
  - mysqli.prepare.md: '« mysqli::prepare'
  - mysqli.real-connect.html: 'mysqli::realconnect »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::query'
---
# mysqli::query

# mysqliquery

(PHP 5, PHP 7, PHP 8)

mysqli::query -- mysqliquery — Виконує запит до бази даних

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

Для не DML-запитів (не INSERT, UPDATE чи DELETE), ця функція рівносильна виклику функції [mysqlirealquery()](mysqli.real-query.html), а потім [mysqliuseresult()](mysqli.use-result.html) або [mysqlistoreresult()](mysqli.store-result.html)

> **Зауваження**
> 
> У випадку, якщо довжина виразу, який ви передаєте в **mysqliquery()**, більше ніж `max_allowed_packet` сервера, коди помилки, що повертаються можуть відрізнятися в залежності від використовуваного драйвера. А це може бути або рідний MySQL драйвер (`mysqlnd`), або клієнтська бібліотека MySQL (`libmysqlclient`). Поведінка функції буде такою:
> 
> -   `mysqlnd` на платформі Linux повертає код помилки 1153. Повідомлення про помилку означає розмір пакета перевищує `max_allowed_packet` байт.
>     
> -   `mysqlnd` на платформі Windows повертає код помилки 2006 року. Це повідомлення про помилку означає відмову сервера.
>     
> -   `libmysqlclient` на всіх платформах повертає код помилки 2006 року. Це повідомлення про помилку означає відмову сервера.
>     

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

`query`

Текст запиту.

**Увага**

# Попередження безпеки: SQL-ін'єкція

Якщо запит містить будь-які вхідні змінні, натомість слід використовувати [запити, що готуються](mysqli.quickstart.prepared-statements.html). Як альтернатива дані повинні бути правильно відформатовані і всі рядки повинні бути екрановані за допомогою функції [mysqlirealescapestring()](mysqli.real-escape-string.html)

`result_mode`

Режим результату може бути однією з трьох констант, що вказують, як результат буде повернено сервером MySQL.

**`MYSQLI_STORE_RESULT`** (за замовчуванням) - повертає об'єкт [mysqliresult](class.mysqli-result.html) із буферизованим набором результатів.

**`MYSQLI_USE_RESULT`** - Повертає об'єкт [mysqliresult](class.mysqli-result.html) із небуферизованим набором результатів. Поки є відкладені записи, що очікують вибірки, лінія з'єднання буде зайнята і всі наступні дзвінки повертатимуть помилку `Commands out of sync`. Щоб уникнути помилки, всі записи повинні бути отримані з сервера або набір результатів має бути відкинуто шляхом виклику [mysqlifreeresult()](mysqli-result.free.html)

**`MYSQLI_ASYNC`** (Доступно з mysqlnd) - запит виконується асинхронно, набір результатів відразу не повертається. Потім використовується [mysqlipoll()](mysqli.poll.md) для отримання результатів за цими запитами. Використовується у поєднанні з константою **`MYSQLI_STORE_RESULT`** або **`MYSQLI_USE_RESULT`**

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. У разі успішного виконання запитів, які створюють набір результатів, таких як `SELECT, SHOW, DESCRIBE` або `EXPLAIN` **mysqliquery()** поверне об'єкт [mysqliresult](class.mysqli-result.html). Для решти успішних запитів **mysqliquery()** поверне **`true`**

### Приклади

**Приклад #1 Приклад використання **mysqli::query()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Создание таблицы, не возвращает набор результатов */
$mysqli->query("CREATE TEMPORARY TABLE myCity LIKE City");
printf("Таблица myCity создана.\n");

/* Запросы SELECT, возвращают набор результатов */
$result = $mysqli->query("SELECT Name FROM City LIMIT 10");
printf("Запрос SELECT вернул %d строк.\n", $result->num_rows);

/* Если нужно извлечь большой объем данных, используем MYSQLI_USE_RESULT */
$result = $mysqli->query("SELECT * FROM City", MYSQLI_USE_RESULT);

/* Важно заметить, что мы не можем вызывать функции, которые взаимодействуют
   с сервером, пока не закроем набор результатов. Все подобные вызовы
   будут вызывать ошибку 'out of sync' */
$mysqli->query("SET @a:='this will not work'");
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Создание таблицы, не возвращает набор результатов */
mysqli_query($link, "CREATE TEMPORARY TABLE myCity LIKE City");
printf("Таблица myCity создана.\n");

/* Запросы SELECT, возвращают набор результатов */
$result = mysqli_query($link, "SELECT Name FROM City LIMIT 10");
printf("Запрос SELECT вернул %d строк.\n", mysqli_num_rows($result));

/* Если нужно извлечь большой объем данных, используем MYSQLI_USE_RESULT */
$result = mysqli_query($link, "SELECT * FROM City", MYSQLI_USE_RESULT);

/* Важно заметить, что мы не можем вызывать функции, которые взаимодействуют
   с сервером, пока не закроем набор результатов. Все подобные вызовы
   будут вызывать ошибку 'out of sync' */
mysqli_query($link, "SET @a:='this will not work'");
```

Результат виконання даних прикладів:

```
Таблица myCity создана.
Запрос SELECT вернул 10 строк.

Fatal error: Uncaught mysqli_sql_exception: Commands out of sync; you can't run this command now in...
```

### Дивіться також

-   [mysqlirealquery()](mysqli.real-query.html) - Виконання SQL запиту
-   [mysqlimultiquery()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних
-   [mysqliprepare()](mysqli.prepare.md) - готує SQL вираз до виконання
-   [mysqlifreeresult()](mysqli-result.free.html) - звільняє пам'ять, зайняту результатами запиту
