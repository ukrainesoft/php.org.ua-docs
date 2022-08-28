Отримує атрибути

-   [« ReflectionClass::export](reflectionclass.export.html)
    
-   [ReflectionClass::getConstant »](reflectionclass.getconstant.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Отримує атрибути
    

# ReflectionClass::getAttributes

(PHP 8)

ReflectionClass::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionClass::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені у цьому класі, у вигляді масиву [ReflectionAttribute](class.reflectionattribute.html)

### Список параметрів

`name`

Фільтрування результатів, щоб залишити лише екземпляри [ReflectionAttribute](class.reflectionattribute.html) для атрибутів, які відповідають цьому імені класу.

`flags`

Прапори для визначення способу фільтрації результатів, якщо вказано параметр `name`

За замовчуванням значення `0`, що повертає результати лише для атрибутів, що належать до класу `name`

Єдиним доступним варіантом є використання константи **`ReflectionAttribute::IS_INSTANCEOF`**яка замість цього буде використовувати для фільтрації `instanceof`

### Значення, що повертаються

Масив атрибутів як об'єкта [ReflectionAttribute](class.reflectionattribute.html)

### Приклади

**Приклад #1 Простий приклад використання**

```php
<?php
#[Attribute]
class Fruit {
}

#[Attribute]
class Red {
}

#[Fruit]
#[Red]
class Apple {
}

$class = new ReflectionClass('Apple');
$attributes = $class->getAttributes();
print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));
?>
```

Результат виконання цього прикладу:

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
class Fruit {
}

#[Attribute]
class Red {
}

#[Fruit]
#[Red]
class Apple {
}

$class = new ReflectionClass('Apple');
$attributes = $class->getAttributes('Fruit');
print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => Fruit
)
```

**Приклад #3 Фільтрування результатів на ім'я класу з наслідуванням**

```php
<?php
interface Color {
}

#[Attribute]
class Fruit {
}

#[Attribute]
class Red implements Colour {
}

#[Fruit]
#[Red]
class Apple {
}

$class = new ReflectionClass('Apple');
$attributes = $class->getAttributes('Colour', ReflectionAttribute::IS_INSTANCEOF);
print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => Red
)
```

### Дивіться також

-   [ReflectionClassConstant::getAttributes()](reflectionclassconstant.getattributes.html) - Отримує атрибути
-   [ReflectionFunctionAbstract::getAttributes()](reflectionfunctionabstract.getattributes.html) - Отримує атрибути
-   [ReflectionParameter::getAttributes()](reflectionparameter.getattributes.html) - Отримує атрибути
-   [ReflectionProperty::getAttributes()](reflectionproperty.getattributes.html) - Отримує атрибути