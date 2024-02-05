---
navigation:
  - class.mysqli-result.md: « mysqli\_result
  - mysqli-result.current-field.md: 'mysqli\_result::$current\_field »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::\_\_construct

(PHP 5, PHP 7, PHP 8)

mysqli\_result::\_\_construct - Конструктор об'єкта [mysqli\_result](class.mysqli-result.md)

### Опис

public **mysqli\_result::\_\_construct** [mysqli](class.mysqli.md) `$mysql`, int`$result_mode` **`MYSQLI_STORE_RESULT`**) .

Метод створює новий об'єкт [mysqli\_result](class.mysqli-result.md)

Метод можна використовувати для створення об'єкту [mysqli\_result](class.mysqli-result.md) після виклику функції [mysqli\_real\_query()](mysqli.real-query.md) або [mysqli\_multi\_query()](mysqli.multi-query.md). Створення об'єкта вручну еквівалентно виклику функції [mysqli\_store\_result()](mysqli.store-result.md) або [mysqli\_use\_result()](mysqli.use-result.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`result_mode`

Режим результату може бути однією з двох констант, що вказують, як результат буде повернуто сервером MySQL:

**`MYSQLI_STORE_RESULT`** (за замовчуванням) - створює об'єкт [mysqli\_result](class.mysqli-result.md) із буферизованим набором результатів.

**`MYSQLI_USE_RESULT`** - Створює об'єкт [mysqli\_result](class.mysqli-result.md) із небуферизованим набором результатів. Поки є очікування вибірки запису, лінія з'єднання буде зайнята і всі наступні дзвінки повертатимуть помилку `Commands out of sync` (Команди не синхронізовані). Щоб уникнути помилки, всі записи повинні бути отримані з сервера або набір результатів має бути відкинуто шляхом виклику функції [mysqli\_free\_result()](mysqli-result.free.md). Для вилучення рядків з'єднання має залишатися відкритим.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Приклад створення об'єкта [mysqli\_result](class.mysqli-result.md)**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* SELECT-запросы возвращают набор результатов */
$mysqli->real_query("SELECT Name FROM City LIMIT 10");

$result = new mysqli_result($mysqli);
printf("Запрос вернул %d записей.\n", $result->num_rows);
```

Висновок наведених прикладів буде схожим на:

```
Запрос вернул 10 записей.
```

### Дивіться також

-   [mysqli\_multi\_query()](mysqli.multi-query.md) \- Виконує один або кілька запитів до бази даних
-   [mysqli\_real\_query()](mysqli.real-query.md) \- Виконання SQL запиту
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
