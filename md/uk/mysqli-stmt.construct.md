---
navigation:
  - mysqli-stmt.close.html: '« mysqlistmt::close'
  - mysqli-stmt.data-seek.html: 'mysqlistmt::dataseek »'
  - index.md: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::construct'
---
# mysqlistmt::construct

(PHP 5, PHP 7, PHP 8)

mysqlistmt::construct — Конструктор для об'єкту [mysqlistmt](class.mysqli-stmt.html)

### Опис

public **mysqlistmt::construct**[mysqli](class.mysqli.md) `$mysql`, ?string `$query` **`null`**

Цей метод створює новий об'єкт класу [mysqlistmt](class.mysqli-stmt.html)

### Список параметрів

`link`

Коректний об'єкт [mysqli](class.mysqli.md)

`query`

Рядок, що містить SQL-запит. Якщо цей параметр **`null`**, то результат буде аналогічним виклику [mysqlistmtinit()](mysqli.stmt-init.html), інакше результат буде аналогічний виклику [mysqliprepare()](mysqli.prepare.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `query` тепер допускає значення null. |

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.md) - готує SQL вираз до виконання
-   [mysqlistmtinit()](mysqli.stmt-init.html) - Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare
