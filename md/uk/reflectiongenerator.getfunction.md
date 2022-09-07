---
navigation:
  - reflectiongenerator.getexecutingline.md: '« ReflectionGenerator::getExecutingLine'
  - reflectiongenerator.getthis.md: 'ReflectionGenerator::getThis »'
  - index.md: PHP Manual
  - class.reflectiongenerator.md: ReflectionGenerator
title: 'ReflectionGenerator::getFunction'
---
# ReflectionGenerator::getFunction

(PHP 7, PHP 8)

ReflectionGenerator::getFunction — Отримати ім'я функції генератора

### Опис

```methodsynopsis
public ReflectionGenerator::getFunction(): ReflectionFunctionAbstract
```

Дозволяє отримати ім'я функції генератора, повертаючи похідний клас від [ReflectionFunctionAbstract](class.reflectionfunctionabstract.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає клас [ReflectionFunctionAbstract](class.reflectionfunctionabstract.md). Може бути [ReflectionFunction](class.reflectionfunction.md) для функцій або [ReflectionMethod](class.reflectionmethod.md) для методів.

### Приклади

**Приклад #1 Приклад використання **ReflectionGenerator::getFunction()****

```php
<?php

function gen()
{
    yield 1;
}

$gen = gen();

$reflectionGen = new ReflectionGenerator($gen);

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

-   [ReflectionGenerator::getThis()](reflectiongenerator.getthis.md) - Отримує значення $this генератора
-   [ReflectionGenerator::getTrace()](reflectiongenerator.gettrace.md) - Отримати трасування запущеного генератора
