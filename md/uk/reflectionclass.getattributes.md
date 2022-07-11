- [« ReflectionClass::export](reflectionclass.export.md)
- [ReflectionClass::getConstant »](reflectionclass.getconstant.md)

- [PHP Manual](index.md)
- [ReflectionClass](class.reflectionclass.md)
- Отримує атрибути

# ReflectionClass::getAttributes

(PHP 8)

ReflectionClass::getAttributes — Отримує атрибути

### Опис

public **ReflectionClass::getAttributes**(?string `$name` = **`null`**,
int `$flags` = 0): array

Повертає всі атрибути, оголошені у цьому класі у вигляді масиву
[ReflectionAttribute](class.reflectionattribute.md).

### Список параметрів

`name`
Фільтрування результатів, щоб залишити лише екземпляри
[ReflectionAttribute](class.reflectionattribute.md) для атрибутів,
відповідних цьому імені класу.

`flags`
Прапори для визначення способу фільтрації результатів, якщо зазначено
параметр `name`.

За замовчуванням значення `0`, яке повертає результати тільки для
атрибутів, що належать до класу `name`.

Єдиним доступним варіантом є використання константи
**`ReflectionAttribute::IS_INSTANCEOF`**, яка натомість буде
використовувати для фільтрації `instanceof`.

### Значення, що повертаються

Масив атрибутів як об'єкта
[ReflectionAttribute](class.reflectionattribute.md).

### Приклади

**Приклад #1 Простий приклад використання**

` <?php#[Attribute]class Fruit {}#[Attribute]class Red {}#[Fruit]#[Red]class Apple {}$class = new ReflectionClass('Apple');$attributes = $class-> getAttributes();print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));?> `

Результат виконання цього прикладу:

Array
(
[0] => Fruit
[1] => Red
)

**Приклад #2 Фільтрування результатів на ім'я класу**

` <?php#[Attribute]class Fruit {}#[Attribute]class Red {}#[Fruit]#[Red]class Apple {}$class = new ReflectionClass('Apple');$attributes = $class-> getAttributes('Fruit');print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));?> `

Результат виконання цього прикладу:

Array
(
[0] => Fruit
)

**Приклад #3 Фільтрування результатів на ім'я класу з наслідуванням**

` <?phpinterface Color {}#[Attribute]class Fruit {}#[Attribute]class Red implements Colour {}#[Fruit]#[Red]class Apple {}$class = new ReflectionClass('Apple' = $class->getAttributes('Colour', ReflectionAttribute::IS_INSTANCEOF);print_r(array_map(fn($attribute) => $attribute->getName(), $attributes));?> `

Результат виконання цього прикладу:

Array
(
[0] => Red
)

### Дивіться також

- [ReflectionClassConstant::getAttributes()](reflectionclassconstant.getattributes.md) -
Отримує атрибути
- [ReflectionFunctionAbstract::getAttributes()](reflectionfunctionabstract.getattributes.md) -
Отримує атрибути
- [ReflectionParameter::getAttributes()](reflectionparameter.getattributes.md) -
Отримує атрибути
- [ReflectionProperty::getAttributes()](reflectionproperty.getattributes.md) -
Отримує атрибути
