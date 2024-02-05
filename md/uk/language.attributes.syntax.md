---
navigation:
  - language.attributes.overview.md: « Введення в атрибути
  - language.attributes.reflection.md: Читання атрибутів за допомогою Reflection API
  - index.md: PHP Manual
  - language.attributes.md: Атрибути
title: Синтаксис атрибутів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Синтаксис атрибутів

Синтаксис атрибутів складається з кількох частин. По-перше, декларація атрибуту починається із символу `#[` і закінчується символом `]`. По-друге, усередині перераховують один або кілька розділених коми атрибутів. Імена атрибутів можуть бути неповними, повними та абсолютними, як описано в розділі [Використання простору імен: основи](language.namespaces.basics.md). Аргументи атрибутів необов'язкові, але якщо вони є, їх укладають у круглі дужки `()`. Аргументи атрибутів може бути або конкретними значеннями (літералами), або константними висловлюваннями. Аргументи можна записувати як позиційним, і іменованим синтаксисом.

Коли Reflection API запитує екземпляр класу атрибута, ім'я атрибута трактується як ім'я класу, що запитується, а аргументи атрибута передаються в конструктор цього класу. Тому для кожного атрибуту потрібно створювати клас.

**Приклад #1 Синтаксис атрибутів**

```php
<?php
// a.php
namespace MyExample;

use Attribute;

#[Attribute]
class MyAttribute
{
    const VALUE = 'value';

    private $value;

    public function __construct($value = null)
    {
        $this->value = $value;
    }
}

// b.php

namespace Another;

use MyExample\MyAttribute;

#[MyAttribute]
#[\MyExample\MyAttribute]
#[MyAttribute(1234)]
#[MyAttribute(value: 1234)]
#[MyAttribute(MyAttribute::VALUE)]
#[MyAttribute(array("key" => "value"))]
#[MyAttribute(100 + 200)]
class Thing
{
}

#[MyAttribute(1234), MyAttribute(5678)]
class AnotherThing
{
}
```
