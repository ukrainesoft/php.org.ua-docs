---
navigation:
  - mysqli.real-escape-string.md: '« mysqli::real\_escape\_string'
  - mysqli.reap-async-query.md: 'mysqli::reap\_async\_query »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::real\_query'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::real\_query

# mysqli\_real\_query

(PHP 5, PHP 7, PHP 8)

mysqli::real\_query -- mysqli\_real\_query — Виконання запиту SQL

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::real_query(string $query): bool
```

Процедурний стиль

```methodsynopsis
mysqli_real_query(mysqli $mysql, string $query): bool
```

Виконує одиночний запит до бази даних, результати якого можна отримати або використовувати функціями [mysqli\_store\_result()](mysqli.store-result.md) або [mysqli\_use\_result()](mysqli.use-result.md)

**Увага**

# Попередження безпеки: SQL-ін'єкція

Замість складання рядку запиту з включенням змінних значень необхідно [готувати запити](mysqli.quickstart.prepared-statements.md). Або рядки запиту мають бути екрановані функцією [mysqli\_real\_escape\_string()](mysqli.real-escape-string.md) та правильно відформатовані.

Щоб визначити, чи має запит повертати результуючий набір, дивіться [mysqli\_field\_count()](mysqli.field-count.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`query`

Текст запиту у вигляді рядка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Дивіться також

-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
