---
navigation:
  - reflectionproperty.setaccessible.md: '« ReflectionProperty::setAccessible'
  - reflectionproperty.tostring.md: 'ReflectionProperty::\_\_toString »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::setValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::setValue

(PHP 5, PHP 7, PHP 8)

ReflectionProperty::setValue — Встановлення значення властивості

### Опис

```methodsynopsis
public ReflectionProperty::setValue(object $object, mixed $value): void
```

```methodsynopsis
public ReflectionProperty::setValue(mixed $value): void
```

Задає (змінює) значення якості.

> **Зауваження**: Починаючи з PHP 8.3.0, виклик цього методу з єдиним аргументом застарів, замість нього необхідно викликати метод [ReflectionClass::setStaticPropertyValue()](reflectionclass.setstaticpropertyvalue.md)

### Список параметрів

`object`

Якщо властивість нестатична, необхідно передати об'єкт, властивість якого потрібно змінити. Якщо властивість статична, *повинно бути*передано значение\*\*`null`\*\*

`value`

Нове значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик цього з єдиним аргументом застарів, замість нього зміни статичного властивості необхідно викликати метод [ReflectionClass::setStaticPropertyValue()](reflectionclass.setstaticpropertyvalue.md) |
| 8.1.0 | Доступ до закритих та захищених властивостей можна відразу ж отримати за допомогою методу [ReflectionProperty::getValue()](reflectionproperty.getvalue.md). . Раніше їх потрібно було зробити за допомогою методу [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.md); в іншому випадку викидався виняток [ReflectionException](class.reflectionexception.md) |

### Приклади

**Пример #1 Пример использования**ReflectionProperty::setValue()\*\*\*\*

```php
<?php
class Foo {
    public static $staticProperty;

    public $property;
    protected $privateProperty;
}

$reflectionClass = new ReflectionClass('Foo');

// С PHP 8.3 больше не нужно вызывать метод setValue для установки значения статического свойства, вместо него необходимо использовать метод setStaticPropertyValue()
$reflectionClass->setStaticPropertyValue('staticProperty', 'foo');
var_dump(Foo::$staticProperty);

$foo = new Foo;

$reflectionClass->getProperty('property')->setValue($foo, 'bar');
var_dump($foo->property);

$reflectionProperty = $reflectionClass->getProperty('privateProperty');
$reflectionProperty->setAccessible(true); // требуется только до PHP 8.1.0
$reflectionProperty->setValue($foo, 'foobar');
var_dump($reflectionProperty->getValue($foo));
?>
```

Результат виконання наведеного прикладу:

```
string(3) "foo"
string(3) "bar"
string(6) "foobar"
```

### Дивіться також

-   [ReflectionProperty::getValue()](reflectionproperty.getvalue.md) \- набуває значення
-   [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.md) \- Робить властивість доступною
-   [ReflectionClass::setStaticPropertyValue()](reflectionclass.setstaticpropertyvalue.md) \- Встановлює значення статичної властивості
