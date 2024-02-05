---
navigation:
  - exception.getmessage.md: '« Exception::getMessage'
  - exception.getcode.md: 'Exception::getCode »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::getPrevious'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Exception::getPrevious

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

Exception::getPrevious — Повертає попередній об'єкт, що реалізує Throwable

### Опис

```methodsynopsis
final public Exception::getPrevious(): ?Throwable
```

Повертає попередній об'єкт, що реалізує [Throwable](class.throwable.md) (переданий третім параметром [Exception::\_\_construct()](exception.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній об'єкт, що реалізує [Throwable](class.throwable.md)или\*\*`null`\*\*якщо такого немає.

### Приклади

**Приклад #1 Приклад використання** Exception::getPrevious()\*\*\*\*

Прохід та друк ланцюга винятків.

```php
<?php
class MyCustomException extends Exception {}

function doStuff() {
    try {
        throw new InvalidArgumentException("Ты делаешь это неправильно!", 112);
    } catch(Exception $e) {
        throw new MyCustomException("Что-то случилось", 911, $e);
    }
}


try {
    doStuff();
} catch(Exception $e) {
    do {
        printf("%s:%d %s (%d) [%s]\n", $e->getFile(), $e->getLine(), $e->getMessage(), $e->getCode(), get_class($e));
    } while($e = $e->getPrevious());
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
/home/bjori/ex.php:8 Что-то случилось (911) [MyCustomException]
/home/bjori/ex.php:6 Ты делаешь это неправильно! (112) [InvalidArgumentException]
```

### Дивіться також

-   [Throwable::getPrevious()](throwable.getprevious.md) \- Повертає попередній Throwable
