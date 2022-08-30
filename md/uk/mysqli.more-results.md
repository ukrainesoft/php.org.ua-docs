Перевірка, чи є ще результати у мультизапиті

-   [« mysqli::kill](mysqli.kill.html)
    
-   [mysqli::multiquery »](mysqli.multi-query.html)
    
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

Вказує, чи є доступні результуючі набори від попереднього виклику функції [mysqlimultiquery()](mysqli.multi-query.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Повертається **`true`** у випадку, якщо один або більше результуючих наборів (включно з помилками) доступні після попереднього виклику функції [mysqlimultiquery()](mysqli.multi-query.html)інакше **`false`**

### Приклади

Дивіться [mysqlimultiquery()](mysqli.multi-query.html)

### Дивіться також

-   [mysqlimultiquery()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних
-   [mysqlinextresult()](mysqli.next-result.html) - Підготовка наступного доступного результуючого набору з multiquery
-   [mysqlistoreresult()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqliuseresult()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання