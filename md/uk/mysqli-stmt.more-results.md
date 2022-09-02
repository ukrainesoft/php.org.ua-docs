---
navigation:
  - mysqli-stmt.insert-id.md: '« mysqlistmt::$insertід'
  - mysqli-stmt.next-result.md: 'mysqlistmt::nextresult »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqlistmt
title: 'mysqlistmt::moreresults'
---
# mysqlistmt::moreresults

# mysqlistmtmoreresults

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqlistmt::moreresults -- mysqlistmtmoreresults — Перевіряє, чи є ще набори рядків через мультизапит.

### Опис

Об'єктно-орієнтований стиль:

```methodsynopsis
public mysqli_stmt::more_results(): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_stmt_more_results(mysqli_stmt $statement): bool
```

Перевіряє, чи є ще набори рядків через мультизапит.

> **Зауваження**
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.md), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`true`**, якщо є доступні результуючі набори, **`false`** в іншому випадку.

### Дивіться також

-   [mysqlistmt::nextresult()](mysqli-stmt.next-result.md) - Читає наступний набір рядків із мультизапиту
-   [mysqli::multiquery()](mysqli.multi-query.md) - Виконує один або кілька запитів до бази даних
