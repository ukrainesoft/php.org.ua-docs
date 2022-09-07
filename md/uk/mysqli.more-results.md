---
navigation:
  - mysqli.kill.md: '« mysqli::kill'
  - mysqli.multi-query.md: 'mysqli::multiquery »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::moreresults'
---
# mysqli::moreresults

# mysqlimoreresults

(PHP 5, PHP 7, PHP 8)

mysqli::moreresults -- mysqlimoreresults — Перевірка, чи є ще результати мультизапиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::more_results(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_more_results(mysqli $mysql): bool
```

Вказує, чи є доступні результуючі набори від попереднього виклику функції [mysqlimultiquery()](mysqli.multi-query.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Повертається **`true`** у випадку, якщо один або більше результуючих наборів (включно з помилками) доступні після попереднього виклику функції [mysqlimultiquery()](mysqli.multi-query.md)інакше **`false`**

### Приклади

Дивіться [mysqlimultiquery()](mysqli.multi-query.md)

### Дивіться також

-   [mysqlimultiquery()](mysqli.multi-query.md) - Виконує один або кілька запитів до бази даних
-   [mysqlinextresult()](mysqli.next-result.md) - Підготовка наступного доступного результуючого набору з multiquery
-   [mysqlistoreresult()](mysqli.store-result.md) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.md) - Готує результуючий набір на сервері для використання
