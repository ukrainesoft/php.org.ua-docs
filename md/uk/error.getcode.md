Повертає код помилки

-   [« Error::getPrevious](error.getprevious.md)
    
-   [Error::getFile »](error.getfile.md)
    
-   [PHP Manual](index.md)
    
-   [Error](class.error.md)
    
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

-   [Throwable::getCode()](throwable.getcode.md) - Повертає код виключення