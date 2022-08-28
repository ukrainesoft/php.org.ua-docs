Отримати запущений об'єкт Generator

-   [« ReflectionGenerator::getExecutingFile](reflectiongenerator.getexecutingfile.html)
    
-   [ReflectionGenerator::getExecutingLine »](reflectiongenerator.getexecutingline.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionGenerator](class.reflectiongenerator.html)
    
-   Отримати запущений об'єкт Generator
    

# ReflectionGenerator::getExecutingGenerator

(PHP 7, PHP 8)

ReflectionGenerator::getExecutingGenerator — Отримати запущений об'єкт [Generator](class.generator.html)

### Опис

```methodsynopsis
public ReflectionGenerator::getExecutingGenerator(): Generator
```

Повертає запущений об'єкт [Generator](class.generator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає запущений об'єкт [Generator](class.generator.html)

### Приклади

**Приклад #1 Приклад використання **ReflectionGenerator::getExecutingGenerator()****

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

$gen2 = $reflectionGen->getExecutingGenerator();

var_dump($gen2 === $gen);
var_dump($gen2->current());
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
int(1);
```

### Дивіться також

-   [ReflectionGenerator::getExecutingLine()](reflectiongenerator.getexecutingline.html) - Отримати поточний рядок генератора, що виконується
-   [ReflectionGenerator::getExecutingFile()](reflectiongenerator.getexecutingfile.html) - Отримати ім'я файлу, з якого запущено генератор