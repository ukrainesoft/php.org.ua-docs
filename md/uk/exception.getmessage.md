Отримує повідомлення виключення

-   [« Exception::\_\_construct](exception.construct.html)
    
-   [Exception::getPrevious »](exception.getprevious.html)
    
-   [PHP Manual](index.html)
    
-   [Exception](class.exception.html)
    
-   Отримує повідомлення виключення
    

# Exception::getMessage

(PHP 5, PHP 7, PHP 8)

Exception::getMessage — Отримує повідомлення про виключення

### Опис

```methodsynopsis
final public Exception::getMessage(): string
```

Повертає повідомлення виключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення виключення у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **Exception::getMessage()****

```php
<?php
try {
    throw new Exception("Какое-нибудь сообщение об ошибке");
} catch(Exception $e) {
    echo $e->getMessage();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Какое-нибудь сообщение об ошибке
```

### Дивіться також

-   [Throwable::getMessage()](throwable.getmessage.html) - Отримує повідомлення помилки