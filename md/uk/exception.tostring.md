Строкове подання винятку

-   [« Exception::getTraceAsString](exception.gettraceasstring.html)
    
-   [Exception::clone »](exception.clone.html)
    
-   [PHP Manual](index.html)
    
-   [Exception](class.exception.html)
    
-   Строкове подання винятку
    

# Exception::function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

Exception::toString — Строкове подання винятку

### Опис

```methodsynopsis
public Exception::__toString(): string
```

Повертає виняток у вигляді рядка (string).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає виняток у вигляді рядка (string).

### Приклади

**Приклад #1 Приклад використання **Exception::toString()****

```php
<?php
try {
    throw new Exception("Какое-нибудь сообщение об ошибке");
} catch(Exception $e) {
    echo $e;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
exception 'Exception' with message 'Какое-нибудь сообщение об ошибке' in /home/bjori/tmp/ex.php:3
Stack trace:
#0 {main}
```

### Дивіться також

-   [Throwable::toString()](throwable.tostring.html) - отримує рядкове подання викинутого об'єкта