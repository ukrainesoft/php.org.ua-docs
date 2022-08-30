Конструктор об'єкту mysqliresult

-   [« mysqliresult](class.mysqli-result.html)
    
-   [mysqliresult::$currentfield »](mysqli-result.current-field.html)
    
-   [PHP Manual](index.md)
    
-   [mysqliresult](class.mysqli-result.html)
    
-   Конструктор об'єкту mysqliresult
    

# mysqliresult::construct

(PHP 5, PHP 7, PHP 8)

mysqliresult::construct - Конструктор об'єкта [mysqliresult](class.mysqli-result.html)

### Опис

public **mysqliresult::construct**[mysqli](class.mysqli.md) `$mysql`, int `$result_mode` **`MYSQLI_STORE_RESULT`**

Метод створює новий об'єкт [mysqliresult](class.mysqli-result.html)

Метод можна використовувати для створення об'єкту [mysqliresult](class.mysqli-result.html) після виклику функції [mysqlirealquery()](mysqli.real-query.html) або [mysqlimultiquery()](mysqli.multi-query.html). Створення об'єкта вручну еквівалентно виклику функції [mysqlistoreresult()](mysqli.store-result.html) або [mysqliuseresult()](mysqli.use-result.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

`result_mode`

Режим результату може бути однією з двох констант, які вказують, як результат буде повернуто сервером MySQL:

**`MYSQLI_STORE_RESULT`** (за замовчуванням) - створює об'єкт [mysqliresult](class.mysqli-result.html) із буферизованим набором результатів.

**`MYSQLI_USE_RESULT`** - Створює об'єкт [mysqliresult](class.mysqli-result.html) із небуферизованим набором результатів. Поки є очікування вибірки запису, лінія з'єднання буде зайнята і всі наступні дзвінки повертатимуть помилку `Commands out of sync` (Команди не синхронізовані). Щоб уникнути помилки, всі записи повинні бути отримані з сервера або набір результатів має бути відкинуто шляхом виклику функції [mysqlifreeresult()](mysqli-result.free.html). Для вилучення рядків з'єднання має залишатися відкритим.

### Приклади

**Приклад #1 Приклад створення об'єкта [mysqliresult](class.mysqli-result.html)**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* SELECT-запросы возвращают набор результатов */
$mysqli->real_query("SELECT Name FROM City LIMIT 10");

$result = new mysqli_result($mysqli);
printf("Запрос вернул %d записей.\n", $result->num_rows);
```

Результатом виконання даних прикладів буде щось подібне:

```
Запрос вернул 10 записей.
```

### Дивіться також

-   [mysqlimultiquery()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних
-   [mysqlirealquery()](mysqli.real-query.html) - Виконання SQL запиту
-   [mysqlistoreresult()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання