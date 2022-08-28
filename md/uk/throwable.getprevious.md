Повертає попередній Throwable

-   [« Throwable::getTraceAsString](throwable.gettraceasstring.html)
    
-   [Throwable::\_\_toString »](throwable.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [Throwable](class.throwable.html)
    
-   Повертає попередній Throwable
    

# Throwable::getPrevious

(PHP 7, PHP 8)

Throwable::getPrevious — Повертає попередній Throwable

### Опис

```methodsynopsis
public Throwable::getPrevious(): ?Throwable
```

Повертає будь-який попередній Throwable (для прикладу, передане третім параметром [Exception::\_\_construct()](exception.construct.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній [Throwable](class.throwable.html), якщо він доступний, або **`null`** в іншому випадку.

### Дивіться також

-   [Exception::getPrevious()](exception.getprevious.html) - Повертає попередній об'єкт, що реалізує Throwable