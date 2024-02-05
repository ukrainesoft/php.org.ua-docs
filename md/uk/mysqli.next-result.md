---
navigation:
  - mysqli.multi-query.md: '« mysqli::multi\_query'
  - mysqli.options.md: 'mysqli::options »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::next\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::next\_result

# mysqli\_next\_result

(PHP 5, PHP 7, PHP 8)

mysqli::next\_result -- mysqli\_next\_result — Підготовка наступного результуючого набору з multi\_query

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::next_result(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_next_result(mysqli $mysql): bool
```

Підготовка наступного доступного результуючого набору попереднього виклику функції [mysqli\_multi\_query()](mysqli.multi-query.md), який потім можна отримати функціями [mysqli\_store\_result()](mysqli.store-result.md) або [mysqli\_use\_result()](mysqli.use-result.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Також повертає **`false`**, якщо наступний оператор призвів до помилки, на відміну від [mysqli\_more\_results()](mysqli.more-results.md)

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

Смотрите[mysqli\_multi\_query()](mysqli.multi-query.md)

### Дивіться також

-   [mysqli\_multi\_query()](mysqli.multi-query.md) \- Виконує один або кілька запитів до бази даних
-   [mysqli\_more\_results()](mysqli.more-results.md) \- Перевірка, чи є ще результати у мультизапиті
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
