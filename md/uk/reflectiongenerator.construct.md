---
navigation:
  - class.reflectiongenerator.md: « ReflectionGenerator
  - reflectiongenerator.getexecutingfile.md: 'ReflectionGenerator::getExecutingFile »'
  - index.md: PHP Manual
  - class.reflectiongenerator.md: ReflectionGenerator
title: 'ReflectionGenerator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionGenerator::\_\_construct

(PHP 7, PHP 8)

ReflectionGenerator::\_\_construct — Конструктор ReflectionGenerator

### Опис

public **ReflectionGenerator::\_\_construct** [Generator](class.generator.md) `$generator`) .

Створює об'єкт [ReflectionGenerator](class.reflectiongenerator.md)

### Список параметрів

`generator`

Об'єкт генератора.

### Приклади

**Приклад #1 Приклад використання** ReflectionGenerator::\_\_construct()\*\*\*\*

```php
<?php

function gen()
{
    yield 1;
}

$gen = gen();

$reflectionGen = new ReflectionGenerator($gen);

echo <<< output
{$reflectionGen->getFunction()->name}
Строка: {$reflectionGen->getExecutingLine()}
Файл: {$reflectionGen->getExecutingFile()}
output;
```

Висновок наведеного прикладу буде схожим на:

```
gen
Строка: 5
Файл: /path/to/file/example.php
```

### Дивіться також

-   [ReflectionGenerator::getFunction()](reflectiongenerator.getfunction.md) \- Отримати ім'я функції генератора
-   [ReflectionGenerator::getExecutingLine()](reflectiongenerator.getexecutingline.md) \- Отримати поточний рядок генератора, що виконується
-   [ReflectionGenerator::getExecutingFile()](reflectiongenerator.getexecutingfile.md) \- Отримати ім'я файлу, з якого запущено генератор
