Отримання імен модифікаторів

-   [« Reflection::export](reflection.export.html)
    
-   [ReflectionClass »](class.reflectionclass.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](class.reflection.html)
    
-   Отримання імен модифікаторів
    

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

**Приклад #1 Приклад використання **Reflection::getModifierNames()****

```php
<?php
class Testing
{
    final public static function foo()
    {
        return;
    }

    public function bar()
    {
        return;
    }
}

$foo = new ReflectionMethod('Testing', 'foo');

echo "Модификаторы для метода foo():\n";
echo $foo->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($foo->getModifiers())) . "\n";

$bar = new ReflectionMethod('Testing', 'bar');

echo "Модификаторы для метода bar():\n";
echo $bar->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($bar->getModifiers()));
```

Результатом виконання цього прикладу буде щось подібне:

```
Модификаторы для метода foo():
261
final public static
Модификаторы для метода bar():
65792
public
```

### Дивіться також

-   [ReflectionClass::getModifiers()](reflectionclass.getmodifiers.html) - Повертає інформацію про модифікаторів класу
-   [ReflectionClassConstant::getModifiers()](reflectionclassconstant.getmodifiers.html) - Отримує модифікатори константи класу
-   [ReflectionMethod::getModifiers()](reflectionmethod.getmodifiers.html) - Отримує модифікатори методу
-   [ReflectionProperty::getModifiers()](reflectionproperty.getmodifiers.html) - Отримання модифікаторів властивостей класу