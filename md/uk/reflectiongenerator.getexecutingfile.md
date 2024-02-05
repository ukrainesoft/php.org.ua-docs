---
navigation:
  - reflectiongenerator.construct.md: '« ReflectionGenerator::\_\_construct'
  - reflectiongenerator.getexecutinggenerator.md: 'ReflectionGenerator::getExecutingGenerator »'
  - index.md: PHP Manual
  - class.reflectiongenerator.md: ReflectionGenerator
title: 'ReflectionGenerator::getExecutingFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionGenerator::getExecutingFile

(PHP 7, PHP 8)

ReflectionGenerator::getExecutingFile — Отримати ім'я файлу, з якого запущено генератор

### Опис

```methodsynopsis
public ReflectionGenerator::getExecutingFile(): string
```

Повертає повний шлях та ім'я файлу поточного запущеного генератора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повний шлях та ім'я файлу поточного запущеного генератора.

### Приклади

**Пример #1 Пример использования**ReflectionGenerator::getExecutingFile()\*\*\*\*

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

echo "Файл: {$reflectionGen->getExecutingFile()}";
```

Висновок наведеного прикладу буде схожим на:

```
Файл: /path/to/file/example.php
```

### Дивіться також

-   [ReflectionGenerator::getExecutingLine()](reflectiongenerator.getexecutingline.md) \- Отримати поточний рядок генератора, що виконується
-   [ReflectionGenerator::getExecutingGenerator()](reflectiongenerator.getexecutinggenerator.md) \- Отримати запущений об'єкт Generator
