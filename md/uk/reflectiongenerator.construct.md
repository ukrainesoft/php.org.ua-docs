Конструктор ReflectionGenerator

-   [« ReflectionGenerator](class.reflectiongenerator.md)
    
-   [ReflectionGenerator::getExecutingFile »](reflectiongenerator.getexecutingfile.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionGenerator](class.reflectiongenerator.md)
    
-   Конструктор ReflectionGenerator
    

# ReflectionGenerator::construct

(PHP 7, PHP 8)

ReflectionGenerator::construct — Конструктор ReflectionGenerator

### Опис

public **ReflectionGenerator::construct**[Generator](class.generator.md) `$generator`

Створює об'єкт [ReflectionGenerator](class.reflectiongenerator.md)

### Список параметрів

`generator`

Об'єкт генератора.

### Приклади

**Приклад #1 Приклад використання **ReflectionGenerator::construct()****

```php
<?php

function gen()
{
    yield 1;
}

$gen = gen();

$reflectionGen = new ReflectionGenerator($gen);

echo <<< output
{$reflectionGen->getFunction()->name}
Строка: {$reflectionGen->getExecutingLine()}
Файл: {$reflectionGen->getExecutingFile()}
output;
```

Результатом виконання цього прикладу буде щось подібне:

```
gen
Строка: 5
Файл: /path/to/file/example.php
```

### Дивіться також

-   [ReflectionGenerator::getFunction()](reflectiongenerator.getfunction.md) - Отримати ім'я функції генератора
-   [ReflectionGenerator::getExecutingLine()](reflectiongenerator.getexecutingline.md) - Отримати поточний рядок генератора, що виконується
-   [ReflectionGenerator::getExecutingFile()](reflectiongenerator.getexecutingfile.md) - Отримати ім'я файлу, з якого запущено генератор