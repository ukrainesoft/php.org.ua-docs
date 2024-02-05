---
navigation:
  - mysqli-stmt.close.md: '« mysqli\_stmt::close'
  - mysqli-stmt.data-seek.md: 'mysqli\_stmt::data\_seek »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::\_\_construct

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::\_\_construct — Конструктор для об'єкту [mysqli\_stmt](class.mysqli-stmt.md)

### Опис

public**mysqli\_stmt::\_\_construct** [mysqli](class.mysqli.md) `$mysql`, ?string`$query` **`null`**) .

Цей метод створює новий об'єкт класу [mysqli\_stmt](class.mysqli-stmt.md)

### Список параметрів

`link`

Коректний об'єкт [mysqli](class.mysqli.md)

`query`

Рядок, що містить SQL-запит. Якщо цей параметр **`null`**, то результат буде аналогічним виклику [mysqli\_stmt\_init()](mysqli.stmt-init.md), інакше результат буде аналогічний виклику [mysqli\_prepare()](mysqli.prepare.md)

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `query` тепер допускає значення null. |

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_init()](mysqli.stmt-init.md) \- Ініціалізує запит та повертає об'єкт для використання у mysqli\_stmt\_prepare
