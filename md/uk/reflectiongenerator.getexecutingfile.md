Отримати ім'я файлу, з якого запущено генератор

-   [« ReflectionGenerator::\_\_construct](reflectiongenerator.construct.html)
    
-   [ReflectionGenerator::getExecutingGenerator »](reflectiongenerator.getexecutinggenerator.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionGenerator](class.reflectiongenerator.html)
    
-   Отримати ім'я файлу, з якого запущено генератор
    

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

**Приклад #1 Приклад використання **ReflectionGenerator::getExecutingFile()****

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

echo "Файл: {$reflectionGen->getExecutingFile()}";
```

Результатом виконання цього прикладу буде щось подібне:

```
Файл: /path/to/file/example.php
```

### Дивіться також

-   [ReflectionGenerator::getExecutingLine()](reflectiongenerator.getexecutingline.html) - Отримати поточний рядок генератора, що виконується
-   [ReflectionGenerator::getExecutingGenerator()](reflectiongenerator.getexecutinggenerator.html) - Отримати запущений об'єкт Generator