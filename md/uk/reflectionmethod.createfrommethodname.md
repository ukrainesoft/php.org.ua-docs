---
navigation:
  - reflectionmethod.construct.md: '« ReflectionMethod::\_\_construct'
  - reflectionmethod.export.md: 'ReflectionMethod::export »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::createFromMethodName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::createFromMethodName

(PHP 8 >= 8.3.0)

ReflectionMethod::createFromMethodName — Створює об'єкт класу ReflectionMethod

### Опис

```methodsynopsis
public static ReflectionMethod::createFromMethodName(string $method): static
```

Створює об'єкт класу [ReflectionMethod](class.reflectionmethod.md)

### Список параметрів

`method`

Імена класу та методу, поділені оператором `::`

### Значення, що повертаються

Повертає новий об'єкт класу [ReflectionMethod](class.reflectionmethod.md) за успішного виконання.

### Помилки

Буде викинуто виняток [ReflectionException](class.reflectionexception.md)якщо заданий метод не існує.

### Приклади

**Пример #1 Пример использования метода**ReflectionMethod::createFromMethodName()\*\*\*\*

```php
<?php

class Foo {
    public function bar() {

    }
}

$methodInfo = ReflectionMethod::createFromMethodName("Foo::bar");
var_dump($methodInfo);
?>
```

Результат виконання наведеного прикладу:

```
object(ReflectionMethod)#1 (2) {
  ["name"]=>
  string(3) "bar"
  ["class"]=>
  string(3) "Foo"
}
```
