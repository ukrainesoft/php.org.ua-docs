---
navigation:
  - reflectionclass.getconstants.md: '« ReflectionClass::getConstants'
  - reflectionclass.getdefaultproperties.md: 'ReflectionClass::getDefaultProperties »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getConstructor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getConstructor

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getConstructor — Повертає конструктор класу

### Опис

```methodsynopsis
public ReflectionClass::getConstructor(): ?ReflectionMethod
```

Повертає конструктор відбитого класу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт [ReflectionMethod](class.reflectionmethod.md), що відображає конструктор класу, або **`null`** якщо клас не має конструктора.

### Приклади

**Пример #1 Пример использования**ReflectionClass::getConstructor()\*\*\*\*

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$constructor = $class->getConstructor();
var_dump($constructor);
?>
```

Результат виконання наведеного прикладу:

```
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(11) "__construct"
  ["class"]=>
  string(15) "ReflectionClass"
}
```

### Дивіться також

-   [ReflectionClass::getName()](reflectionclass.getname.md) \- Повертає ім'я класу
