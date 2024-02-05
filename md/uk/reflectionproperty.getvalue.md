---
navigation:
  - reflectionproperty.gettype.md: '« ReflectionProperty::getType'
  - reflectionproperty.hasdefaultvalue.md: 'ReflectionProperty::hasDefaultValue »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::getValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Якщо властивість не статична, необхідно передати об'єкт, з якого потрібно отримати цю властивість. Якщо вам потрібно отримати властивість за умовчанням, не надаючи об'єкта, використовуйте функцію [ReflectionClass::getDefaultProperties()](reflectionclass.getdefaultproperties.md)

### Значення, що повертаються

Поточне значення якості.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Доступ до закритих та захищених властивостей можна відразу ж отримати за допомогою методу **ReflectionProperty::getValue()**. . Раніше їх потрібно було зробити за допомогою методу [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.md); в іншому випадку викидався виняток [ReflectionException](class.reflectionexception.md) |
| 8.0.0 | `object` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** ReflectionProperty::getValue()\*\*\*\*

```php
<?php
class Foo {
    public static $staticProperty = 'foobar';

    public $property = 'barfoo';
    protected $privateProperty = 'foofoo';
}

$reflectionClass = new ReflectionClass('Foo');

var_dump($reflectionClass->getProperty('staticProperty')->getValue());
var_dump($reflectionClass->getProperty('property')->getValue(new Foo));

$reflectionProperty = $reflectionClass->getProperty('privateProperty');
$reflectionProperty->setAccessible(true); // требуется только до PHP 8.1.0
var_dump($reflectionProperty->getValue(new Foo));
?>
```

Результат виконання наведеного прикладу:

```
string(6) "foobar"
string(6) "barfoo"
string(6) "foofoo"
```

### Дивіться також

-   [ReflectionProperty::setValue()](reflectionproperty.setvalue.md) \- Встановлення значення якості
-   [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.md) \- Робить властивість доступною
-   [ReflectionClass::getDefaultProperties()](reflectionclass.getdefaultproperties.md) \- Повертає властивості за промовчанням
-   [ReflectionClass::getStaticPropertyValue()](reflectionclass.getstaticpropertyvalue.md) \- Повертає значення статичної властивості
