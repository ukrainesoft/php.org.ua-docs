---
navigation:
  - function.method-exists.md: « methodexists
  - function.trait-exists.md: traitexists »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: propertyexists
---
# propertyexists

(PHP 5> = 5.1.0, PHP 7, PHP 8)

propertyexists — Перевіряє, чи об'єкт або клас містить зазначений атрибут.

### Опис

```methodsynopsis
property_exists(object|string $object_or_class, string $property): bool
```

Функція перевіряє, чи існує атрибут `property` у вказаному класі.

> **Зауваження**
> 
> В протилежність [isset()](function.isset.md) **propertyexists()** повертає \*\*`true`\*\*навіть якщо властивість має значення **`null`**

### Список параметрів

`object_or_class`

Ім'я класу або об'єкт класу для перевірки

`property`

Ім'я якості

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо властивість існує, \*\*`false`\*\*якщо воно не існує, або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **propertyexists()****

```php
<?php

class myClass {
    public $mine;
    private $xpto;
    static protected $test;

    static function test() {
        var_dump(property_exists('myClass', 'xpto')); //true
    }
}

var_dump(property_exists('myClass', 'mine'));   //true
var_dump(property_exists(new myClass, 'mine')); //true
var_dump(property_exists('myClass', 'xpto'));   //true
var_dump(property_exists('myClass', 'bar'));    //false
var_dump(property_exists('myClass', 'test'));   //true
myClass::test();

?>
```

### Примітки

> **Зауваження**
> 
> Виклик цієї функції буде використовувати всі зареєстровані [функции автозагрузки](language.oop5.autoload.md)якщо клас ще не відомий.

> **Зауваження**
> 
> Функція **propertyexists()** не визначає магічно доступні властивості за допомогою методу [`__get`](language.oop5.overloading.md#language.oop5.overloading.members)

### Дивіться також

-   [methodexists()](function.method-exists.md) - Перевіряє, чи існує метод у даному класі
