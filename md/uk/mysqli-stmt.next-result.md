---
navigation:
  - mysqli-stmt.more-results.md: '« mysqlistmt::moreresults'
  - mysqli-stmt.num-rows.md: 'mysqlistmt::$numrows »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqlistmt
title: 'mysqlistmt::nextresult'
---
# mysqlistmt::nextresult

# mysqlistmtnextresult

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqlistmt::nextresult -- mysqlistmtnextresult — Читає наступний набір рядків із мультизапиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::next_result(): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_stmt_next_result(mysqli_stmt $statement): bool
```

Читає наступний набір рядків із мультизапиту.

> **Зауваження**
> 
> До PHP 8.1.0, функція доступна лише з [mysqlnd](book.mysqlnd.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.md), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер також доступно при збиранні з libmysqlclient. |

### Дивіться також

-   [mysqlistmt::moreresults()](mysqli-stmt.more-results.md) - Перевіряє, чи є ще набори рядків внаслідок мультизапиту
-   [mysqli::multiquery()](mysqli.multi-query.md) - Виконує один або кілька запитів до бази даних
