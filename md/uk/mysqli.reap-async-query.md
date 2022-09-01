---
navigation:
  - mysqli.real-query.html: '« mysqli::realquery'
  - mysqli.refresh.md: 'mysqli::refresh »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::reapasyncquery'
---
# mysqli::reapasyncquery

# mysqlireapasyncquery

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqli::reapasyncquery -- mysqlireapasyncquery — Отримання результату асинхронного запиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::reap_async_query(): mysqli_result|bool
```

Процедурний стиль

```methodsynopsis
mysqli_reap_async_query(mysqli $mysql): mysqli_result|bool
```

Отримує результат асинхронного запиту.

> **Зауваження**
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. Для успішних запитів, які виробляють набір результатів, таких як `SELECT, SHOW, DESCRIBE` або `EXPLAIN` **mysqlireapasyncquery()** поверне об'єкт [mysqliresult](class.mysqli-result.html). Для інших успішних запитів **mysqlireapasyncquery()** поверне **`true`**

### Дивіться також

-   [mysqlipoll()](mysqli.poll.md) - Опитування підключень
