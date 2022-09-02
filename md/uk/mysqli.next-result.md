---
navigation:
  - mysqli.multi-query.md: '« mysqli::multiquery'
  - mysqli.options.md: 'mysqli::options »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::nextresult'
---
# mysqli::nextresult

# mysqlinextresult

(PHP 5, PHP 7, PHP 8)

mysqli::nextresult -- mysqlinextresult — Підготовка наступного результуючого набору з multiquery

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::next_result(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_next_result(mysqli $mysql): bool
```

Підготовка наступного доступного результуючого набору попереднього виклику функції [mysqlimultiquery()](mysqli.multi-query.md), який потім можна отримати функціями [mysqlistoreresult()](mysqli.store-result.md) або [mysqliuseresult()](mysqli.use-result.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Також повертає **`false`**, якщо наступний оператор призвів до помилки, на відміну від [mysqlimoreresults()](mysqli.more-results.md)

### Приклади

Дивіться [mysqlimultiquery()](mysqli.multi-query.md)

### Дивіться також

-   [mysqlimultiquery()](mysqli.multi-query.md) - Виконує один або кілька запитів до бази даних
-   [mysqlimoreresults()](mysqli.more-results.md) - Перевірка, чи є ще результати у мультизапиті
-   [mysqlistoreresult()](mysqli.store-result.md) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.md) - Готує результуючий набір на сервері для використання
