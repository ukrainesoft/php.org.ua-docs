---
navigation:
  - reflection.export.md: '« Reflection::export'
  - class.reflectionclass.md: ReflectionClass »
  - index.md: PHP Manual
  - class.reflection.md: Reflection
title: 'Reflection::getModifierNames'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Reflection::getModifierNames

(PHP 5, PHP 7, PHP 8)

Reflection::getModifierNames — Отримання імен модифікаторів

### Опис

```methodsynopsis
public static Reflection::getModifierNames(int $modifiers): array
```

Отримує імена модифікаторів.

### Список параметрів

`modifiers`

Бітова маска модифікаторів.

### Значення, що повертаються

Масив імен модифікаторів.

### Приклади

**Пример #1 Пример использования**Reflection::getModifierNames()\*\*\*\*

```php
<?php
class Testing
{
    final public static function foo()
    {
        return;
    }

    public function bar()
    {
        return;
    }
}

$foo = new ReflectionMethod('Testing', 'foo');

echo "Модификаторы для метода foo():\n";
echo $foo->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($foo->getModifiers())) . "\n";

$bar = new ReflectionMethod('Testing', 'bar');

echo "Модификаторы для метода bar():\n";
echo $bar->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($bar->getModifiers()));
```

Висновок наведеного прикладу буде схожим на:

```
Модификаторы для метода foo():
261
final public static
Модификаторы для метода bar():
65792
public
```

### Дивіться також

-   [ReflectionClass::getModifiers()](reflectionclass.getmodifiers.md) \- Повертає інформацію про модифікаторів класу
-   [ReflectionClassConstant::getModifiers()](reflectionclassconstant.getmodifiers.md) \- Отримує модифікатори константи класу
-   [ReflectionMethod::getModifiers()](reflectionmethod.getmodifiers.md) \- Отримує модифікатори методу
-   [ReflectionProperty::getModifiers()](reflectionproperty.getmodifiers.md) \- Отримання модифікаторів властивостей класу
