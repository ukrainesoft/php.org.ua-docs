---
navigation:
  - language.attributes.syntax.html: « Синтаксис атрибутів
  - language.attributes.classes.html: Оголошення класів атрибутів »
  - index.html: PHP Manual
  - language.attributes.html: Атрибути
title: Читання атрибутів за допомогою Reflection API
---
## Читання атрибутів за допомогою Reflection API

Для доступу до атрибутів класів, методів, функцій, параметрів, властивостей та констант класу, в Reflection API присутній метод **getAttributes()** для кожного з цих об'єктів рефлексії. Цей метод повертає масив екземплярів [ReflectionAttribute](class.reflectionattribute.html), у кожного з яких можна запросити ім'я атрибуту та його аргументи, а також створити об'єкт, який представляє атрибут.

Таке відокремлення властивостей атрибута від створення об'єкта дає програмісту більш повний контроль над обробкою помилок, пов'язаних з відсутнім класом атрибуту і некоректністю його аргументів. Об'єкт атрибуту буде створено та перевірено на коректність аргументів лише після виклику [ReflectionAttribute::newInstance()](reflectionattribute.newinstance.html), не раніше.

**Приклад #1 Читання атрибутів за допомогою Reflection API**

```php
<?php

#[Attribute]
class MyAttribute
{
    public $value;

    public function __construct($value)
    {
        $this->value = $value;
    }
}

#[MyAttribute(value: 1234)]
class Thing
{
}

function dumpAttributeData($reflection) {
    $attributes = $reflection->getAttributes();

    foreach ($attributes as $attribute) {
       var_dump($attribute->getName());
       var_dump($attribute->getArguments());
       var_dump($attribute->newInstance());
    }
}

dumpAttributeData(new ReflectionClass(Thing::class));
/*
string(11) "MyAttribute"
array(1) {
  ["value"]=>
  int(1234)
}
object(MyAttribute)#3 (1) {
  ["value"]=>
  int(1234)
}
*/
```

Замість того, щоб послідовно перебирати всі атрибути об'єкта рефлексії, можна вказати ім'я класу як аргумент і отримати лише відповідні атрибути.

**Приклад #2 Читання конкретних атрибутів за допомогою Reflection API**

```php
<?php

function dumpMyAttributeData($reflection) {
    $attributes = $reflection->getAttributes(MyAttribute::class);

    foreach ($attributes as $attribute) {
       var_dump($attribute->getName());
       var_dump($attribute->getArguments());
       var_dump($attribute->newInstance());
    }
}

dumpMyAttributeData(new ReflectionClass(Thing::class));
```
