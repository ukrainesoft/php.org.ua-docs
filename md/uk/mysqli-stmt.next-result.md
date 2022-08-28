Читає наступний набір рядків із мультизапиту

-   [« mysqli\_stmt::more\_results](mysqli-stmt.more-results.html)
    
-   [mysqli\_stmt::$num\_rows »](mysqli-stmt.num-rows.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Читає наступний набір рядків із мультизапиту
    

# mysqlistmt::nextresult

# mysqlistmtnextresult

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqlistmt::nextresult -- mysqlistmtnextresult — Читає наступний набір рядків із мультизапиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::next_result(): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_stmt_next_result(mysqli_stmt $statement): bool
```

Читає наступний набір рядків із мультизапиту.

> **Зауваження**
> 
> До PHP 8.1.0, функція доступна лише з [mysqlnd](book.mysqlnd.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер також доступно при збиранні з libmysqlclient. |

### Дивіться також

-   [mysqli\_stmt::more\_results()](mysqli-stmt.more-results.html) - Перевіряє, чи є ще набори рядків внаслідок мультизапиту
-   [mysqli::multi\_query()](mysqli.multi-query.html) - Виконує один або кілька запитів до бази даних