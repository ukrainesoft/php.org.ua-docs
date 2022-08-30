Повертає попередній Throwable

-   [« Error::getMessage](error.getmessage.md)
    
-   [Error::getCode »](error.getcode.md)
    
-   [PHP Manual](index.md)
    
-   [Error](class.error.md)
    
-   Повертає попередній Throwable
    

# Error::getPrevious

(PHP 7, PHP 8)

Error::getPrevious — Повертає попередній Throwable

### Опис

```methodsynopsis
final public Error::getPrevious(): ?Throwable
```

Повертає попередній об'єкт Throwable (третій параметр конструктора [Error::construct()](error.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній об'єкт [Throwable](class.throwable.md), якщо він є, і \*\*`null`\*\*якщо його немає.

### Приклади

**Приклад #1 Приклад використання **Error::getPrevious()****

Прохід та друк ланцюга винятків.

```php
<?php
class MyCustomError extends Error {}

function doStuff() {
    try {
        throw new InvalidArgumentError("Вы делаете это неправильно!", 112);
    } catch(Error $e) {
        throw new MyCustomError("Что-то случилось", 911, $e);
    }
}


try {
    doStuff();
} catch(Error $e) {
    do {
        printf("%s:%d %s (%d) [%s]\n", $e->getFile(), $e->getLine(), $e->getMessage(), $e->getCode(), get_class($e));
    } while($e = $e->getPrevious());
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/home/bjori/ex.php:8 Что-то случилось (911) [MyCustomError]
/home/bjori/ex.php:6 Вы делаете это неправильно! (112) [InvalidArgumentError]
```

### Дивіться також

-   [Throwable::getPrevious()](throwable.getprevious.md) - Повертає попередній Throwable