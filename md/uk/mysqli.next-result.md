Підготовка наступного доступного результуючого набору з multiquery

-   [« mysqli::multi\_query](mysqli.multi-query.html)
    
-   [mysqli::options »](mysqli.options.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Підготовка наступного доступного результуючого набору з multiquery
    

# mysqli::nextresult

# mysqlinextresult

(PHP 5, PHP 7, PHP 8)

mysqli::nextresult -- mysqlinextresult — Підготовка наступного результуючого набору з multiquery

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::next_result(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_next_result(mysqli $mysql): bool
```

Підготовка наступного доступного результуючого набору попереднього виклику функції [mysqli\_multi\_query()](mysqli.multi-query.html), який потім можна отримати функціями [mysqli\_store\_result()](mysqli.store-result.html) або [mysqli\_use\_result()](mysqli.use-result.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Також повертає **`false`**, якщо наступний оператор призвів до помилки, на відміну від [mysqli\_more\_results()](mysqli.more-results.html)

### Приклади

Дивіться [mysqli\_multi\_query()](mysqli.multi-query.html)

### Дивіться також

-   [mysqli\_multi\_query()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних
-   [mysqli\_more\_results()](mysqli.more-results.html) - Перевірка, чи є ще результати у мультизапиті
-   [mysqli\_store\_result()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання