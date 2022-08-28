Отримати значення, що повертається генератором

-   [« Generator::current](generator.current.html)
    
-   [Generator::key »](generator.key.html)
    
-   [PHP Manual](index.html)
    
-   [Generator](class.generator.html)
    
-   Отримати значення, що повертається генератором
    

# Generator::getReturn

(PHP 7, PHP 8)

Generator::getReturn — Отримати значення, що повертається генератором

### Опис

```methodsynopsis
public Generator::getReturn(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Отримує значення генератора, що повертається, після його завершення.

### Приклади

**Приклад #1 Приклад використання **Generator::getReturn()****

```php
<?php

$gen = (function() {
    yield 1;
    yield 2;

    return 3;
})();

foreach ($gen as $val) {
    echo $val, PHP_EOL;
}

echo $gen->getReturn(), PHP_EOL;
```

Результат виконання цього прикладу:

```
1
2
3
```