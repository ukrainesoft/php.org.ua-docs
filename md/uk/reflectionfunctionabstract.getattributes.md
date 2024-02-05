---
navigation:
  - reflectionfunctionabstract.clone.md: '« ReflectionFunctionAbstract::\_\_clone'
  - reflectionfunctionabstract.getclosurescopeclass.md: 'ReflectionFunctionAbstract::getClosureScopeClass »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getAttributes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getAttributes

(PHP 8)

ReflectionFunctionAbstract::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені для цієї функції або методу у вигляді масиву [ReflectionAttribute](class.reflectionattribute.md)

### Список параметрів

`name`

Фільтрування результатів, щоб залишити лише екземпляри [ReflectionAttribute](class.reflectionattribute.md) для атрибутів, які відповідають цьому імені класу.

`flags`

Флаги для определения способа фильтрации результатов, если указан параметр`name`

По умолчанию значение , що повертає результати лише для атрибутів, що належать до класу `name`

Єдиним доступним варіантом є використання константи \*\*`ReflectionAttribute::IS_INSTANCEOF`\*\*яка замість цього буде використовувати для фільтрації `instanceof`

### Значення, що повертаються

Масив атрибутів як об'єкта [ReflectionAttribute](class.reflectionattribute.md)

### Приклади

**Приклад #1 Простий приклад із методом класу**

```php
<?php
#[Attribute]
class Fruit {
}

#[Attribute]
class Red {
}

class Factory {
    #[Fruit]
    #[Red]
    public function makeApple(): string
    {
        return 'apple';
    }
}

$method = new ReflectionMethod('Factory', 'makeApple');
$attributes = $method->getAttributes();
print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Fruit
    [1] => Red
)
```

**Приклад #2 Простий приклад із функцією**

```php
<?php
#[Attribute]
class Fruit {
}

#[Attribute]
class Red {
}

#[Fruit]
#[Red]
function makeApple(): string
{
    return 'apple';
}

$function = new ReflectionFunction('makeApple');
$attributes = $function->getAttributes();
print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Fruit
    [1] => Red
)
```

**Приклад #3 Фільтрування результатів на ім'я класу**

```php
<?php
#[Attribute]
class Fruit {
}

#[Attribute]
class Red {
}

#[Fruit]
#[Red]
function makeApple(): string
{
    return 'apple';
}

$function = new ReflectionFunction('makeApple');
$attributes = $function->getAttributes('Fruit');
print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Fruit
)
```

**Приклад #4 Фільтрування результатів на ім'я класу, з успадкуванням**

```php
<?php
interface Color {
}

#[Attribute]
class Fruit {
}

#[Attribute]
class Red implements Color {
}

#[Fruit]
#[Red]
function makeApple(): string
{
    return 'apple';
}

$function = new ReflectionFunction('makeApple');
$attributes = $function->getAttributes('Color', ReflectionAttribute::IS_INSTANCEOF);
print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Red
)
```

### Дивіться також

-   [ReflectionClass::getAttributes()](reflectionclass.getattributes.md) \- Отримує атрибути
-   [ReflectionClassConstant::getAttributes()](reflectionclassconstant.getattributes.md) \- Отримує атрибути
-   [ReflectionParameter::getAttributes()](reflectionparameter.getattributes.md) \- Отримує атрибути
-   [ReflectionProperty::getAttributes()](reflectionproperty.getattributes.md) \- Отримує атрибути
