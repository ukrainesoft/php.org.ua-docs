---
navigation:
  - function.method-exists.md: « method\_exists
  - function.trait-exists.md: trait\_exists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: property\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# property\_exists

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

property\_exists — Перевіряє, чи об'єкт чи клас атрибут міститься

### Опис

```methodsynopsis
property_exists(object|string $object_or_class, string $property): bool
```

Функція перевіряє, чи існує атрибут `property` у вказаному класі.

> **Зауваження** :
> 
> На противагу мовній конструкції [isset()](function.isset.md), функция**property\_exists()** повертає \*\*`true`\*\*навіть якщо значення властивості дорівнює **`null`**

### Список параметрів

`object_or_class`

Ім'я класу чи об'єкт класу для перевірки.

`property`

Ім'я якості.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо властивість існує, \*\*`false`\*\*якщо не існує.

### Приклади

**Пример #1 Пример использования функции**property\_exists()\*\*\*\*

```php
<?php

class myClass {
    public $mine;
    private $xpto;
    static protected $test;

    static function test() {
        var_dump(property_exists('myClass', 'xpto')); //true
    }
}

var_dump(property_exists('myClass', 'mine'));   //true
var_dump(property_exists(new myClass, 'mine')); //true
var_dump(property_exists('myClass', 'xpto'));   //true
var_dump(property_exists('myClass', 'bar'));    //false
var_dump(property_exists('myClass', 'test'));   //true
myClass::test();

?>
```

### Примітки

> **Зауваження** :
> 
> Виклик цієї функції буде використовувати всі зареєстровані [функції автозавантаження](language.oop5.autoload.md)якщо клас ще не відомий.

> **Зауваження** :
> 
> Функция**property\_exists()** не визначає властивості, які магічно доступні через магічний метод [`__get`](language.oop5.overloading.md#language.oop5.overloading.members)

### Дивіться також

-   [method\_exists()](function.method-exists.md) \- Перевіряє, чи існує метод у даному класі
