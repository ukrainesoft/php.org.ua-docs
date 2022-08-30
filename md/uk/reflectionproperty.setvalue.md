Встановлення значення якості

-   [« ReflectionProperty::setAccessible](reflectionproperty.setaccessible.html)
    
-   [ReflectionProperty::toString »](reflectionproperty.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionProperty](class.reflectionproperty.html)
    
-   Встановлення значення якості
    

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

### Список параметрів

`object`

Якщо властивість нестатична, необхідно передати об'єкт, властивість якого потрібно змінити. Якщо властивість статична, цей аргумент пропускається, і потрібно задати лише `value`

`value`

Нове значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [ReflectionException](class.reflectionexception.html)якщо властивість недоступна. Можна робити захищені та закриті властивості доступними за допомогою [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.html)

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::setValue()****

```php
<?php
class Foo {
    public static $staticProperty;

    public $property;
    protected $privateProperty;
}

$reflectionClass = new ReflectionClass('Foo');

$reflectionClass->getProperty('staticProperty')->setValue('foo');
var_dump(Foo::$staticProperty);

$foo = new Foo;

$reflectionClass->getProperty('property')->setValue($foo, 'bar');
var_dump($foo->property);

$reflectionProperty = $reflectionClass->getProperty('privateProperty');
$reflectionProperty->setAccessible(true);
$reflectionProperty->setValue($foo, 'foobar');
var_dump($reflectionProperty->getValue($foo));
?>
```

Результат виконання цього прикладу:

```
string(3) "foo"
string(3) "bar"
string(6) "foobar"
```

### Дивіться також

-   [ReflectionProperty::getValue()](reflectionproperty.getvalue.html) - набуває значення
-   [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.html) - Робить властивість доступною
-   [ReflectionClass::setStaticPropertyValue()](reflectionclass.setstaticpropertyvalue.html) - Встановлює значення статичної властивості