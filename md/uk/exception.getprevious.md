Повертає попередній об'єкт, що реалізує Throwable

-   [« Exception::getMessage](exception.getmessage.html)
    
-   [Exception::getCode »](exception.getcode.html)
    
-   [PHP Manual](index.html)
    
-   [Exception](class.exception.html)
    
-   Повертає попередній об'єкт, що реалізує Throwable
    

# Exception::getPrevious

(PHP 5> = 5.3.0, PHP 7, PHP 8)

Exception::getPrevious — Повертає попередній об'єкт, що реалізує Throwable

### Опис

```methodsynopsis
final public Exception::getPrevious(): ?Throwable
```

Повертає попередній об'єкт, що реалізує [Throwable](class.throwable.html) (переданий третім параметром [Exception::\_\_construct()](exception.construct.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній об'єкт, що реалізує [Throwable](class.throwable.html) або **`null`**якщо такого немає.

### Приклади

**Приклад #1 Приклад використання **Exception::getPrevious()****

Прохід та друк ланцюга винятків.

```php
<?php
class MyCustomException extends Exception {}

function doStuff() {
    try {
        throw new InvalidArgumentException("Ты делаешь это неправильно!", 112);
    } catch(Exception $e) {
        throw new MyCustomException("Что-то случилось", 911, $e);
    }
}


try {
    doStuff();
} catch(Exception $e) {
    do {
        printf("%s:%d %s (%d) [%s]\n", $e->getFile(), $e->getLine(), $e->getMessage(), $e->getCode(), get_class($e));
    } while($e = $e->getPrevious());
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/home/bjori/ex.php:8 Что-то случилось (911) [MyCustomException]
/home/bjori/ex.php:6 Ты делаешь это неправильно! (112) [InvalidArgumentException]
```

### Дивіться також

-   [Throwable::getPrevious()](throwable.getprevious.html) - Повертає попередній Throwable