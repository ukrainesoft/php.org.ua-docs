Повертає код помилки

-   [« Error::getPrevious](error.getprevious.html)
    
-   [Error::getFile »](error.getfile.html)
    
-   [PHP Manual](index.html)
    
-   [Error](class.error.html)
    
-   Повертає код помилки
    

# Error::getCode

(PHP 7, PHP 8)

Error::getCode — Повертає код помилки

### Опис

```methodsynopsis
final public Error::getCode(): int
```

Повертає код помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код помилки типу int

### Приклади

**Приклад #1 Приклад використання**Error::getCode()\*\*\*\*

```php
<?php
try {
    throw new Error("Какое-то сообщение об ошибке", 30);
} catch(Error $e) {
    echo "Код ошибки: " . $e->getCode();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Код ошибки: 30
```

### Дивіться також

-   [Throwable::getCode()](throwable.getcode.html) - Повертає код виключення