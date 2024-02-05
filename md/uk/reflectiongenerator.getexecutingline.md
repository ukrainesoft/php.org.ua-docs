---
navigation:
  - reflectiongenerator.getexecutinggenerator.md: '« ReflectionGenerator::getExecutingGenerator'
  - reflectiongenerator.getfunction.md: 'ReflectionGenerator::getFunction »'
  - index.md: PHP Manual
  - class.reflectiongenerator.md: ReflectionGenerator
title: 'ReflectionGenerator::getExecutingLine'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionGenerator::getExecutingLine

(PHP 7, PHP 8)

ReflectionGenerator::getExecutingLine — Отримати поточний рядок генератора, що виконується.

### Опис

```methodsynopsis
public ReflectionGenerator::getExecutingLine(): int
```

Повертає поточний рядок генератора, що виконується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер поточного рядка генератора, що виконується.

### Приклади

**Пример #1 Пример использования**ReflectionGenerator::getExecutingLine()\*\*\*\*

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

echo "Строка: {$reflectionGen->getExecutingLine()}";
```

Висновок наведеного прикладу буде схожим на:

```
Строка: 7
```

### Дивіться також

-   [ReflectionGenerator::getExecutingGenerator()](reflectiongenerator.getexecutinggenerator.md) \- Отримати запущений об'єкт Generator
-   [ReflectionGenerator::getExecutingFile()](reflectiongenerator.getexecutingfile.md) \- Отримати ім'я файлу, з якого запущено генератор
