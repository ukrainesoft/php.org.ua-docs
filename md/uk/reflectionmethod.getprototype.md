---
navigation:
  - reflectionmethod.getmodifiers.md: '« ReflectionMethod::getModifiers'
  - reflectionmethod.hasprototype.md: 'ReflectionMethod::hasPrototype »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::getPrototype'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::getPrototype

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

ReflectionMethod::getPrototype — Отримує прототип методу (якщо такий є)

### Опис

```methodsynopsis
public ReflectionMethod::getPrototype(): ReflectionMethod
```

Отримує прототип методу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт [ReflectionMethod](class.reflectionmethod.md)прототипа метода.

### Помилки

Исключение[ReflectionException](class.reflectionexception.md) викидається, якщо метод не має прототипу.

### Приклади

**Пример #1 Пример использования**ReflectionMethod::getPrototype()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(10) "sayHelloTo"
  ["class"]=>
  string(5) "Hello"
}
```

### Дивіться також

-   [ReflectionMethod::getModifiers()](reflectionmethod.getmodifiers.md) \- Отримує модифікатори методу
-   [ReflectionMethod::hasPrototype()](reflectionmethod.hasprototype.md) \- Визначає, чи має метод прототип
