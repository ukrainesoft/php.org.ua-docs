---
navigation:
  - reflectiongenerator.getfunction.md: '« ReflectionGenerator::getFunction'
  - reflectiongenerator.gettrace.md: 'ReflectionGenerator::getTrace »'
  - index.md: PHP Manual
  - class.reflectiongenerator.md: ReflectionGenerator
title: 'ReflectionGenerator::getThis'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionGenerator::getThis

(PHP 7, PHP 8)

ReflectionGenerator::getThis — Получает значение`$this`генератора

### Опис

```methodsynopsis
public ReflectionGenerator::getThis(): ?object
```

Получить значение`$this`, До якого має доступ генератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає значення `$this`или\*\*`null`\*\*якщо генератор створений поза контекстом класу.

### Приклади

**Приклад #1 Приклад використання** ReflectionGenerator::getThis()\*\*\*\*

```php
<?php

class GenExample
{
    public function gen()
    {
        yield 1;
    }
}

$gen = (new GenExample)->gen();

$reflectionGen = new ReflectionGenerator($gen);

var_dump($reflectionGen->getThis());
```

Висновок наведеного прикладу буде схожим на:

```
object(GenExample)#3 (0) {
}
```

### Дивіться також

-   [ReflectionGenerator::getFunction()](reflectiongenerator.getfunction.md) \- Отримати ім'я функції генератора
-   [ReflectionGenerator::getTrace()](reflectiongenerator.gettrace.md) \- Отримати трасування запущеного генератора
