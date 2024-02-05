---
navigation:
  - reflectionproperty.export.md: '« ReflectionProperty::export'
  - reflectionproperty.getdeclaringclass.md: 'ReflectionProperty::getDeclaringClass »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::getAttributes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::getAttributes

(PHP 8)

ReflectionProperty::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionProperty::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені в цій властивості класу, у вигляді масиву [ReflectionAttribute](class.reflectionattribute.md)

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

**Приклад #1 Простий приклад**

```php
<?php
#[Attribute]
class Fruit {
}

#[Attribute]
class Red {
}

class Basket {
    #[Fruit]
    #[Red]
    public string $apple = 'apple';
}

$property = new ReflectionProperty('Basket', 'apple');
$attributes = $property->getAttributes();
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

**Приклад #2 Фільтрування результатів на ім'я класу**

```php
<?php
#[Attribute]
class Fruit {
}

#[Attribute]
class Red {
}

class Basket {
    #[Fruit]
    #[Red]
    public string $apple = 'apple';
}

$property = new ReflectionProperty('Basket', 'apple');
$attributes = $property->getAttributes('Fruit');
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

**Приклад #3 Фільтрування результатів на ім'я класу, з успадкуванням**

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

class Basket {
    #[Fruit]
    #[Red]
    public string $apple = 'apple';
}

$property = new ReflectionProperty('Basket', 'apple');
$attributes = $property->getAttributes('Color', ReflectionAttribute::IS_INSTANCEOF);
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
-   [ReflectionFunctionAbstract::getAttributes()](reflectionfunctionabstract.getattributes.md) \- Отримує атрибути
-   [ReflectionParameter::getAttributes()](reflectionparameter.getattributes.md) \- Отримує атрибути
