---
navigation:
  - language.attributes.syntax.md: « Синтаксис атрибутів
  - language.attributes.classes.md: Оголошення класів атрибутів »
  - index.md: PHP Manual
  - language.attributes.md: Атрибути
title: Читання атрибутів за допомогою Reflection API
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Читання атрибутів за допомогою Reflection API

Для доступу до атрибутів класів, методів, функцій, параметрів, властивостей та констант класу в Reflection API існує метод \*\*getAttributes()\*\*що визначено для кожного з перерахованих об'єктів рефлексії. Цей метод повертає масив об'єктів [ReflectionAttribute](class.reflectionattribute.md), у кожного з яких можна запросити ім'я та аргументи, а також створити об'єкт класу, який представляє атрибут.

Відділення отриманого через рефлексію уявлення атрибута від явного створення об'єкта дає програмісту повніший контроль над обробкою помилок, пов'язаних з відсутніми класами атрибутів, друкарськими помилками або відсутніми аргументами. Об'єкт класу атрибуту буде створено та перевірено на коректність аргументів лише після виклику методу [ReflectionAttribute::newInstance()](reflectionattribute.newinstance.md), не раніше.

**Приклад #1 Читання атрибутів засобами Reflection API**

```php
<?php

#[Attribute]
class MyAttribute
{
    public $value;

    public function __construct($value)
    {
        $this->value = $value;
    }
}

#[MyAttribute(value: 1234)]
class Thing
{
}

function dumpAttributeData($reflection) {
    $attributes = $reflection->getAttributes();

    foreach ($attributes as $attribute) {
       var_dump($attribute->getName());
       var_dump($attribute->getArguments());
       var_dump($attribute->newInstance());
    }
}

dumpAttributeData(new ReflectionClass(Thing::class));
/*
string(11) "MyAttribute"
array(1) {
  ["value"]=>
  int(1234)
}
object(MyAttribute)#3 (1) {
  ["value"]=>
  int(1234)
}
*/
```

Щоб отримати атрибути тільки потрібного класу, замість послідовного перебору всіх атрибутів об'єкта рефлексії метод **getAttributes()** передають як аргумент ім'я шуканого класу атрибута.

**Приклад #2 Читання конкретних атрибутів засобами Reflection API**

```php
<?php

function dumpMyAttributeData($reflection) {
    $attributes = $reflection->getAttributes(MyAttribute::class);

    foreach ($attributes as $attribute) {
       var_dump($attribute->getName());
       var_dump($attribute->getArguments());
       var_dump($attribute->newInstance());
    }
}

dumpMyAttributeData(new ReflectionClass(Thing::class));
```
