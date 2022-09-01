---
navigation:
  - mysqli.multi-query.html: '« mysqli::multiquery'
  - mysqli.options.html: 'mysqli::options »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
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

Підготовка наступного доступного результуючого набору попереднього виклику функції [mysqlimultiquery()](mysqli.multi-query.html), який потім можна отримати функціями [mysqlistoreresult()](mysqli.store-result.html) або [mysqliuseresult()](mysqli.use-result.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Також повертає **`false`**, якщо наступний оператор призвів до помилки, на відміну від [mysqlimoreresults()](mysqli.more-results.html)

### Приклади

Дивіться [mysqlimultiquery()](mysqli.multi-query.html)

### Дивіться також

-   [mysqlimultiquery()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних
-   [mysqlimoreresults()](mysqli.more-results.html) - Перевірка, чи є ще результати у мультизапиті
-   [mysqlistoreresult()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання
