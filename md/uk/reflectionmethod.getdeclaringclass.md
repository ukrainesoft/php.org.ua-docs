---
navigation:
  - reflectionmethod.getclosure.md: '« ReflectionMethod::getClosure'
  - reflectionmethod.getmodifiers.md: 'ReflectionMethod::getModifiers »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::getDeclaringClass'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::getDeclaringClass

(PHP 5, PHP 7, PHP 8)

ReflectionMethod::getDeclaringClass — Отримує клас, що оголошує відображений метод

### Опис

```methodsynopsis
public ReflectionMethod::getDeclaringClass(): ReflectionClass
```

Отримує клас, що оголошує відбитий метод.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт класу [ReflectionClass](class.reflectionclass.md)частиною якого є відбитий метод.

### Приклади

**Пример #1 Пример использования**ReflectionMethod::getDeclaringClass()\*\*\*\*

```php
<?php
class HelloWorld {

    protected function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod(new HelloWorld(), 'sayHelloTo');
var_dump($reflectionMethod->getDeclaringClass());
?>
```

Результат виконання наведеного прикладу:

```
object(ReflectionClass)#2 (1) {
  ["name"]=>
  string(10) "HelloWorld"
}
```

### Дивіться також

-   [ReflectionMethod::isAbstract()](reflectionmethod.isabstract.md) \- Перевіряє, чи є метод абстрактним
