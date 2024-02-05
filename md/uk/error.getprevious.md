---
navigation:
  - error.getmessage.md: '« Error::getMessage'
  - error.getcode.md: 'Error::getCode »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::getPrevious'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::getPrevious

(PHP 7, PHP 8)

Error::getPrevious — Повертає попередній Throwable

### Опис

```methodsynopsis
final public Error::getPrevious(): ?Throwable
```

Повертає попередній об'єкт Throwable (третій параметр конструктора [Error::\_\_construct()](error.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає попередній об'єкт [Throwable](class.throwable.md), якщо він є, і \*\*`null`\*\*якщо його немає.

### Приклади

**Пример #1 Пример использования**Error::getPrevious()\*\*\*\*

Прохід та друк ланцюга винятків.

```php
<?php
class MyCustomError extends Error {}

function doStuff() {
    try {
        throw new InvalidArgumentError("Вы делаете это неправильно!", 112);
    } catch(Error $e) {
        throw new MyCustomError("Что-то случилось", 911, $e);
    }
}


try {
    doStuff();
} catch(Error $e) {
    do {
        printf("%s:%d %s (%d) [%s]\n", $e->getFile(), $e->getLine(), $e->getMessage(), $e->getCode(), get_class($e));
    } while($e = $e->getPrevious());
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
/home/bjori/ex.php:8 Что-то случилось (911) [MyCustomError]
/home/bjori/ex.php:6 Вы делаете это неправильно! (112) [InvalidArgumentError]
```

### Дивіться також

-   [Throwable::getPrevious()](throwable.getprevious.md) \- Повертає попередній Throwable
