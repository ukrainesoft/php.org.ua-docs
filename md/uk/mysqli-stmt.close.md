Закриває підготовлений запит

-   [« mysqli\_stmt::bind\_result](mysqli-stmt.bind-result.html)
    
-   [mysqli\_stmt::\_\_construct »](mysqli-stmt.construct.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Закриває підготовлений запит
    

# mysqlistmt::close

# mysqlistmtclose

(PHP 5, PHP 7, PHP 8)

mysqlistmt::close -- mysqlistmtclose — Закриває підготовлений запит

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::close(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_close(mysqli_stmt $statement): bool
```

Закриває підготовлений запит . **mysqlistmtclose()** також звільняє дескриптор запиту. Якщо за поточним запитом отримано результат, ця функція очищає його для того, щоб міг бути виконаний наступний запит.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.html) - готує SQL вираз до виконання