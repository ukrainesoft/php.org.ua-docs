Перевіряє, чи є ще набори рядків через мультизапит.

-   [« mysqlistmt::$insertід](mysqli-stmt.insert-id.html)
    
-   [mysqlistmt::nextresult »](mysqli-stmt.next-result.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlistmt](class.mysqli-stmt.html)
    
-   Перевіряє, чи є ще набори рядків через мультизапит.
    

# mysqlistmt::moreresults

# mysqlistmtmoreresults

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqlistmt::moreresults -- mysqlistmtmoreresults — Перевіряє, чи є ще набори рядків через мультизапит.

### Опис

Об'єктно-орієнтований стиль:

```methodsynopsis
public mysqli_stmt::more_results(): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_stmt_more_results(mysqli_stmt $statement): bool
```

Перевіряє, чи є ще набори рядків через мультизапит.

> **Зауваження**
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає **`true`**, якщо є доступні результуючі набори, **`false`** в іншому випадку.

### Дивіться також

-   [mysqlistmt::nextresult()](mysqli-stmt.next-result.html) - Читає наступний набір рядків із мультизапиту
-   [mysqli::multiquery()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних