---
navigation:
  - language.attributes.overview.html: « Введення в атрибути
  - language.attributes.reflection.html: Чтение атрибутов с помощью Reflection API »
  - index.html: PHP Manual
  - language.attributes.html: Атрибути
title: Синтаксис атрибутів
---
## Синтаксис атрибутів

Синтаксис атрибутів складається із кількох частин. Для початку декларація атрибуту завжди починається із символу `#[` і закінчується `]`. Усередині перерахування з одного або більше розділених комою атрибутів. Атрибути можна задавати за допомогою неповних, повних та абсолютних імен, як описано в розділі [Використання простору імен: основи](language.namespaces.basics.html). Аргументи атрибутів опціональні, але якщо вони є, то полягають у дужках `()`. Аргументи атрибутів можуть бути або конкретними значеннями або константними виразами. Для аргументів можна використовувати як позиційний синтаксис, і синтаксис іменованих аргументів.

Коли атрибут запитується за допомогою Reflection API, його ім'я трактується як ім'я класу, а аргументи передаються його конструктор. Таким чином, для кожного атрибуту має існувати відповідний клас.

**Приклад #1 Синтаксис атрибутів**

```php
<?php
// a.php
namespace MyExample;

use Attribute;

#[Attribute]
class MyAttribute
{
    const VALUE = 'value';

    private $value;

    public function __construct($value = null)
    {
        $this->value = $value;
    }
}

// b.php

namespace Another;

use MyExample\MyAttribute;

#[MyAttribute]
#[\MyExample\MyAttribute]
#[MyAttribute(1234)]
#[MyAttribute(value: 1234)]
#[MyAttribute(MyAttribute::VALUE)]
#[MyAttribute(array("key" => "value"))]
#[MyAttribute(100 + 200)]
class Thing
{
}

#[MyAttribute(1234), MyAttribute(5678)]
class AnotherThing
{
}
```
