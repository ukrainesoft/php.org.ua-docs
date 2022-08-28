Конструктор об'єкту mysqliresult

-   [« mysqli\_result](class.mysqli-result.html)
    
-   [mysqli\_result::$current\_field »](mysqli-result.current-field.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_result](class.mysqli-result.html)
    
-   Конструктор об'єкту mysqliresult
    

# mysqliresult::construct

(PHP 5, PHP 7, PHP 8)

mysqliresult::construct - Конструктор об'єкта [mysqli\_result](class.mysqli-result.html)

### Опис

public **mysqliresult::construct**[mysqli](class.mysqli.html) `$mysql`, int `$result_mode` **`MYSQLI_STORE_RESULT`**

Метод створює новий об'єкт [mysqli\_result](class.mysqli-result.html)

Метод можна використовувати для створення об'єкту [mysqli\_result](class.mysqli-result.html) після виклику функції [mysqli\_real\_query()](mysqli.real-query.html) або [mysqli\_multi\_query()](mysqli.multi-query.html). Створення об'єкта вручну еквівалентно виклику функції [mysqli\_store\_result()](mysqli.store-result.html) або [mysqli\_use\_result()](mysqli.use-result.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`result_mode`

Режим результату може бути однією з двох констант, які вказують, як результат буде повернуто сервером MySQL:

**`MYSQLI_STORE_RESULT`** (за замовчуванням) - створює об'єкт [mysqli\_result](class.mysqli-result.html) із буферизованим набором результатів.

**`MYSQLI_USE_RESULT`** - Створює об'єкт [mysqli\_result](class.mysqli-result.html) із небуферизованим набором результатів. Поки є очікування вибірки запису, лінія з'єднання буде зайнята і всі наступні дзвінки повертатимуть помилку `Commands out of sync` (Команди не синхронізовані). Щоб уникнути помилки, всі записи повинні бути отримані з сервера або набір результатів має бути відкинуто шляхом виклику функції [mysqli\_free\_result()](mysqli-result.free.html). Для вилучення рядків з'єднання має залишатися відкритим.

### Приклади

**Приклад #1 Приклад створення об'єкта [mysqli\_result](class.mysqli-result.html)**

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

-   [mysqli\_multi\_query()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних
-   [mysqli\_real\_query()](mysqli.real-query.html) - Виконання SQL запиту
-   [mysqli\_store\_result()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання