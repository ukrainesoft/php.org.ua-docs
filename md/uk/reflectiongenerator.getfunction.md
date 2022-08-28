Отримати ім'я функції генератора

-   [« ReflectionGenerator::getExecutingLine](reflectiongenerator.getexecutingline.html)
    
-   [ReflectionGenerator::getThis »](reflectiongenerator.getthis.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionGenerator](class.reflectiongenerator.html)
    
-   Отримати ім'я функції генератора
    

# ReflectionGenerator::getFunction

(PHP 7, PHP 8)

ReflectionGenerator::getFunction — Отримати ім'я функції генератора

### Опис

```methodsynopsis
public ReflectionGenerator::getFunction(): ReflectionFunctionAbstract
```

Дозволяє отримати ім'я функції генератора, повертаючи похідний клас від [ReflectionFunctionAbstract](class.reflectionfunctionabstract.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає клас [ReflectionFunctionAbstract](class.reflectionfunctionabstract.html). Може бути [ReflectionFunction](class.reflectionfunction.html) для функцій або [ReflectionMethod](class.reflectionmethod.html) для методів.

### Приклади

**Приклад #1 Приклад використання **ReflectionGenerator::getFunction()****

```php
<?php

function gen()
{
    yield 1;
}

$gen = gen();

$reflectionGen = new ReflectionGenerator($gen);

var_dump($reflectionGen->getFunction());
```

Результатом виконання цього прикладу буде щось подібне:

```
object(ReflectionFunction)#3 (1) {
  ["name"]=>
  string(3) "gen"
}
```

### Дивіться також

-   [ReflectionGenerator::getThis()](reflectiongenerator.getthis.html) - Отримує значення $this генератора
-   [ReflectionGenerator::getTrace()](reflectiongenerator.gettrace.html) - Отримати трасування запущеного генератора