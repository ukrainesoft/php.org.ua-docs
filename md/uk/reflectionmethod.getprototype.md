---
navigation:
  - reflectionmethod.getmodifiers.md: '« ReflectionMethod::getModifiers'
  - reflectionmethod.invoke.md: 'ReflectionMethod::invoke »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::getPrototype'
---
# ReflectionMethod::getPrototype

(PHP 5> = 5.1.2, PHP 7, PHP 8)

ReflectionMethod::getPrototype — Отримує прототип методу (якщо такий є)

### Опис

```methodsynopsis
public ReflectionMethod::getPrototype(): ReflectionMethod
```

Отримує прототип методу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт [ReflectionMethod](class.reflectionmethod.md) методу прототипу.

### Помилки

Виняток [ReflectionException](class.reflectionexception.md) викидається, якщо метод не має прототипу.

### Приклади

**Приклад #1 Приклад використання **ReflectionMethod::getPrototype()****

```php
<?php
class Hello {

    public function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}
class HelloWorld extends Hello {

    public function sayHelloTo($name) {
        return 'Привет, мир: ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
var_dump($reflectionMethod->getPrototype());
?>
```

Результат виконання цього прикладу:

```
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(10) "sayHelloTo"
  ["class"]=>
  string(5) "Hello"
}
```

### Дивіться також

-   [ReflectionMethod::getModifiers()](reflectionmethod.getmodifiers.md) - Отримує модифікатори методу
