Звільняє пам'ять, зайняту результатами запиту

-   [« mysqli\_result::field\_seek](mysqli-result.field-seek.html)
    
-   [mysqli\_result::getIterator »](mysqli-result.getiterator.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_result](class.mysqli-result.html)
    
-   Звільняє пам'ять, зайняту результатами запиту
    

# mysqliresult::free

# mysqliresult::close

# mysqliresult::freeresult

# mysqlifreeresult

(PHP 5, PHP 7, PHP 8)

mysqliresult::free -- mysqliresult::close -- mysqliresult::freeresult -- mysqlifreeresult — Звільняє пам'ять, зайняту результатами запиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::free(): void
```

```methodsynopsis
public mysqli_result::close(): void
```

```methodsynopsis
public mysqli_result::free_result(): void
```

Процедурний стиль

```methodsynopsis
mysqli_free_result(mysqli_result $result): void
```

Визволяє пам'ять, зайняту результатами запиту.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.html), отриманий за допомогою [mysqli\_query()](mysqli.query.html) [mysqli\_store\_result()](mysqli.store-result.html) [mysqli\_use\_result()](mysqli.use-result.html) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mysqli\_query()](mysqli.query.html) - Виконує запит до бази даних
-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html) - Отримує результат із підготовленого запиту у вигляді об'єкта mysqliresult
-   [mysqli\_store\_result()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.html) - Готує результуючий набір на сервері для використання