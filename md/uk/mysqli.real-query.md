Виконання SQL запиту

-   [« mysqli::real\_escape\_string](mysqli.real-escape-string.html)
    
-   [mysqli::reap\_async\_query »](mysqli.reap-async-query.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Виконання SQL запиту
    

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

Виконує одиночний запит до бази даних, результати якого можна отримати або використовувати функціями [mysqli\_store\_result()](mysqli.store-result.html) або [mysqli\_use\_result()](mysqli.use-result.html)

Щоб визначити, чи має запит повертати результуючий набір, дивіться [mysqli\_field\_count()](mysqli.field-count.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`query`

Текст запиту у вигляді рядка.

**Увага**

# Попередження безпеки: SQL-ін'єкція

Якщо запит містить будь-які вхідні змінні, натомість слід використовувати [подготавливаемые запросы](mysqli.quickstart.prepared-statements.html). Як альтернатива дані повинні бути правильно відформатовані і всі рядки повинні бути екрановані за допомогою функції [mysqli\_real\_escape\_string()](mysqli.real-escape-string.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqli\_query()](mysqli.query.html) - Виконує запит до бази даних
-   [mysqli\_store\_result()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання