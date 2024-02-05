---
navigation:
  - reflectionclass.getinterfaces.md: '« ReflectionClass::getInterfaces'
  - reflectionclass.getmethods.md: 'ReflectionClass::getMethods »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getMethod'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getMethod

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getMethod — Повертає екземпляр [ReflectionMethod](class.reflectionmethod.md)для метода класса

### Опис

```methodsynopsis
public ReflectionClass::getMethod(string $name): ReflectionMethod
```

Повертає екземпляр [ReflectionMethod](class.reflectionmethod.md)для метода класса.

### Список параметрів

`name`

Досліджуваний метод.

### Значення, що повертаються

Екземпляр класу [ReflectionMethod](class.reflectionmethod.md)

### Помилки

[ReflectionException](class.reflectionexception.md) якщо метод не існує.

### Приклади

**Пример #1 Пример использования**ReflectionClass::getMethod()\*\*\*\*

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$method = $class->getMethod('getMethod');
var_dump($method);
?>
```

Результат виконання наведеного прикладу:

```
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(9) "getMethod"
  ["class"]=>
  string(15) "ReflectionClass"
}
```

### Дивіться також

-   [ReflectionClass::getMethods()](reflectionclass.getmethods.md) \- Повертає список методів у вигляді масиву
