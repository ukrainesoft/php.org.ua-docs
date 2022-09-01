---
navigation:
  - mysqli.real-escape-string.html: '« mysqli::realescapestring'
  - mysqli.reap-async-query.html: 'mysqli::reapasyncquery »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
title: 'mysqli::realquery'
---
# mysqli::realquery

# mysqlirealquery

(PHP 5, PHP 7, PHP 8)

mysqli::realquery -- mysqlirealquery — Виконання запиту SQL

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::real_query(string $query): bool
```

Процедурний стиль

```methodsynopsis
mysqli_real_query(mysqli $mysql, string $query): bool
```

Виконує одиночний запит до бази даних, результати якого можна отримати або використовувати функціями [mysqlistoreresult()](mysqli.store-result.html) або [mysqliuseresult()](mysqli.use-result.md)

Щоб визначити, чи має запит повертати результуючий набір, дивіться [mysqlifieldcount()](mysqli.field-count.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

`query`

Текст запиту у вигляді рядка.

**Увага**

# Попередження безпеки: SQL-ін'єкція

Якщо запит містить будь-які вхідні змінні, натомість слід використовувати [запити, що готуються](mysqli.quickstart.prepared-statements.html). Як альтернатива дані повинні бути правильно відформатовані і всі рядки повинні бути екрановані за допомогою функції [mysqlirealescapestring()](mysqli.real-escape-string.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqliquery()](mysqli.query.md) - Виконує запит до бази даних
-   [mysqlistoreresult()](mysqli.store-result.md) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.md) - Готує результуючий набір на сервері для використання
