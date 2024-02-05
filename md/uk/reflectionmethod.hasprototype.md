---
navigation:
  - reflectionmethod.getprototype.md: '« ReflectionMethod::getPrototype'
  - reflectionmethod.invoke.md: 'ReflectionMethod::invoke »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::hasPrototype'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::hasPrototype

(PHP 8 >= 8.2.0)

ReflectionMethod::hasPrototype — Визначає, чи є метод прототип

### Опис

```methodsynopsis
public ReflectionMethod::hasPrototype(): bool
```

Визначає, чи має метод прототип.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** якщо метод має прототип, інакше повертає **`false`**

### Приклади

**Пример #1 Пример использования**ReflectionMethod::hasPrototype()\*\*\*\*

```php
<?php

class Hello
{
    public function sayHelloTo($name)
    {
        return 'Hello '.$name;
    }
}

class HelloWorld extends Hello
{
    public function sayHelloTo($name)
    {
        return 'Hello world: '.$name;
    }
}
$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
var_dump($reflectionMethod->hasPrototype());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionMethod::getPrototype()](reflectionmethod.getprototype.md) \- Отримує прототип методу (якщо такий є)
