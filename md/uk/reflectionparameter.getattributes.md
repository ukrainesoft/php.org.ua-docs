---
navigation:
  - reflectionparameter.export.md: '« ReflectionParameter::export'
  - reflectionparameter.getclass.md: 'ReflectionParameter::getClass »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::getAttributes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::getAttributes

(PHP 8)

ReflectionParameter::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionParameter::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені в цьому параметрі у вигляді масиву [ReflectionAttribute](class.reflectionattribute.md)

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

function fruitBasket(
   #[Fruit]
   #[Red]
   string $apple
) { }

$reflection = new ReflectionFunction('fruitBasket');
$parameter = $reflection->getParameter('apple');
$attributes = $parameter->getAttributes();
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

function fruitBasket(
   #[Fruit]
   #[Red]
   string $apple
) { }

$reflection = new ReflectionFunction('fruitBasket');
$parameter = $reflection->getParameter('apple');
$attributes = $parameter->getAttributes('Fruit');
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

function fruitBasket(
   #[Fruit]
   #[Red]
   string $apple
) { }

$reflection = new ReflectionFunction('fruitBasket');
$parameter = $reflection->getParameter('apple');
$attributes = $parameter->getAttributes('Color', ReflectionAttribute::IS_INSTANCEOF);
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
-   [ReflectionProperty::getAttributes()](reflectionproperty.getattributes.md) \- Отримує атрибути
