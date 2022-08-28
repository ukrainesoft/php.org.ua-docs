Отримує значення $this генератора

-   [« ReflectionGenerator::getFunction](reflectiongenerator.getfunction.html)
    
-   [ReflectionGenerator::getTrace »](reflectiongenerator.gettrace.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionGenerator](class.reflectiongenerator.html)
    
-   Отримує значення $this генератора
    

# ReflectionGenerator::getThis

(PHP 7, PHP 8)

ReflectionGenerator::getThis — Отримує значення `$this` генератора

### Опис

```methodsynopsis
public ReflectionGenerator::getThis(): ?object
```

Отримати значення `$this`, До якого має доступ генератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає значення `$this` або **`null`**якщо генератор створений поза контекстом класу.

### Приклади

**Приклад #1 Приклад використання **ReflectionGenerator::getThis()****

```php
<?php

class GenExample
{
    public function gen()
    {
        yield 1;
    }
}

$gen = (new GenExample)->gen();

$reflectionGen = new ReflectionGenerator($gen);

var_dump($reflectionGen->getThis());
```

Результатом виконання цього прикладу буде щось подібне:

```
object(GenExample)#3 (0) {
}
```

### Дивіться також

-   [ReflectionGenerator::getFunction()](reflectiongenerator.getfunction.html) - Отримати ім'я функції генератора
-   [ReflectionGenerator::getTrace()](reflectiongenerator.gettrace.html) - Отримати трасування запущеного генератора