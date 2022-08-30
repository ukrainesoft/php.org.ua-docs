Отримання результату асинхронного запиту

-   [« mysqli::realquery](mysqli.real-query.html)
    
-   [mysqli::refresh »](mysqli.refresh.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Отримання результату асинхронного запиту
    

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
> Доступно лише з модулем [mysqlnd](book.mysqlnd.html)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Повертає **`false`** у разі виникнення помилки. Для успішних запитів, які виробляють набір результатів, таких як `SELECT, SHOW, DESCRIBE` або `EXPLAIN` **mysqlireapasyncquery()** поверне об'єкт [mysqliresult](class.mysqli-result.html). Для інших успішних запитів **mysqlireapasyncquery()** поверне **`true`**

### Дивіться також

-   [mysqlipoll()](mysqli.poll.html) - Опитування підключень