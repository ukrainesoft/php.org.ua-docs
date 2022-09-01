---
navigation:
  - reflectionproperty.gettype.html: '« ReflectionProperty::getType'
  - reflectionproperty.hasdefaultvalue.html: 'ReflectionProperty::hasDefaultValue »'
  - index.html: PHP Manual
  - class.reflectionproperty.html: ReflectionProperty
title: 'ReflectionProperty::getValue'
---
# ReflectionProperty::getValue

(PHP 5, PHP 7, PHP 8)

ReflectionProperty::getValue — Отримує значення

### Опис

```methodsynopsis
public ReflectionProperty::getValue(?object $object = null): mixed
```

Отримує значення якості.

### Список параметрів

`object`

Якщо властивість не статична, необхідно передати об'єкт, з якого потрібно отримати цю властивість. Якщо вам потрібно отримати властивість за промовчанням, не надаючи об'єкта, використовуйте функцію [ReflectionClass::getDefaultProperties()](reflectionclass.getdefaultproperties.html)

### Значення, що повертаються

Поточне значення якості.

### Помилки

Викидає виняток [ReflectionException](class.reflectionexception.html)якщо властивість недоступна. Захищені та закриті властивості можна зробити доступними функцією [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | `object` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::getValue()****

```php
<?php
class Foo {
    public static $staticProperty = 'foobar';

    public $property = 'barfoo';
    protected $privateProperty = 'foofoo';
}

$reflectionClass = new ReflectionClass('Foo');

var_dump($reflectionClass->getProperty('staticProperty')->getValue());
var_dump($reflectionClass->getProperty('property')->getValue(new Foo));

$reflectionProperty = $reflectionClass->getProperty('privateProperty');
$reflectionProperty->setAccessible(true);
var_dump($reflectionProperty->getValue(new Foo));
?>
```

Результат виконання цього прикладу:

```
string(6) "foobar"
string(6) "barfoo"
string(6) "foofoo"
```

### Дивіться також

-   [ReflectionProperty::setValue()](reflectionproperty.setvalue.html) - Встановлення значення якості
-   [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.html) - Робить властивість доступною
-   [ReflectionClass::getDefaultProperties()](reflectionclass.getdefaultproperties.html) - Повертає властивості за промовчанням
-   [ReflectionClass::getStaticPropertyValue()](reflectionclass.getstaticpropertyvalue.html) - Повертає значення статичної властивості
