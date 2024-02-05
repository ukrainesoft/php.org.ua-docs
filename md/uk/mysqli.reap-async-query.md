---
navigation:
  - mysqli.real-query.md: '« mysqli::real\_query'
  - mysqli.refresh.md: 'mysqli::refresh »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::reap\_async\_query'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::reap\_async\_query

# mysqli\_reap\_async\_query

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

mysqli::reap\_async\_query -- mysqli\_reap\_async\_query — Отримання результату асинхронного запиту

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

> **Зауваження** :
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. Для успішних запитів, які виробляють набір результатів, таких як `SELECT, SHOW, DESCRIBE`или`EXPLAIN` **mysqli\_reap\_async\_query()** поверне об'єкт [mysqli\_result](class.mysqli-result.md). Для інших успішних запитів **mysqli\_reap\_async\_query()** поверне **`true`**

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Дивіться також

-   [mysqli\_poll()](mysqli.poll.md) \- Опитування підключень
