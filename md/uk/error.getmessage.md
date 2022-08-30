Отримує повідомлення про помилку

-   [« Error::construct](error.construct.html)
    
-   [Error::getPrevious »](error.getprevious.html)
    
-   [PHP Manual](index.html)
    
-   [Error](class.error.html)
    
-   Отримує повідомлення про помилку
    

# Error::getMessage

(PHP 7, PHP 8)

Error::getMessage — Отримує повідомлення про помилку

### Опис

```methodsynopsis
final public Error::getMessage(): string
```

Повертає повідомлення про помилку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **Error::getMessage()****

```php
<?php
try {
    throw new Error("Страшная ошибка");
} catch(Error $e) {
    echo $e->getMessage();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Страшная ошибка
```

### Дивіться також

-   [Throwable::getMessage()](throwable.getmessage.html) - Отримує повідомлення помилки