Перевірка, чи є ще результати у мультизапиті

-   [« mysqli::kill](mysqli.kill.html)
    
-   [mysqli::multi\_query »](mysqli.multi-query.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Перевірка, чи є ще результати у мультизапиті
    

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

Вказує, чи є доступні результуючі набори від попереднього виклику функції [mysqli\_multi\_query()](mysqli.multi-query.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

### Значення, що повертаються

Повертається **`true`** у випадку, якщо один або більше результуючих наборів (включно з помилками) доступні після попереднього виклику функції [mysqli\_multi\_query()](mysqli.multi-query.html)інакше **`false`**

### Приклади

Дивіться [mysqli\_multi\_query()](mysqli.multi-query.html)

### Дивіться також

-   [mysqli\_multi\_query()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних
-   [mysqli\_next\_result()](mysqli.next-result.html) - Підготовка наступного доступного результуючого набору з multiquery
-   [mysqli\_store\_result()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання