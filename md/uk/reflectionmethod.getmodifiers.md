---
navigation:
  - reflectionmethod.getdeclaringclass.md: '« ReflectionMethod::getDeclaringClass'
  - reflectionmethod.getprototype.md: 'ReflectionMethod::getPrototype »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::getModifiers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::getModifiers

(PHP 5, PHP 7, PHP 8)

ReflectionMethod::getModifiers — Отримує модифікатори методу

### Опис

```methodsynopsis
public ReflectionMethod::getModifiers(): int
```

Повертає бітове поле модифікаторів доступу методу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числове уявлення модифікаторів. Описи та значення цих модифікаторів наведено у списку [зумовлених констант](class.reflectionmethod.md#reflectionmethod.constants.modifiers)

### Приклади

**Приклад #1 Приклад використання** ReflectionMethod::getModifiers()\*\*\*\*

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

echo "Модификаторы метода foo():\n";
echo $foo->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($foo->getModifiers())) . "\n";

$bar = new ReflectionMethod('Testing', 'bar');

echo "Модификаторы метода bar():\n";
echo $bar->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($bar->getModifiers()));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Модификаторы метода foo():
49
final public static
Модификаторы метода bar():
1
public
```

### Дивіться також

-   [Reflection::getModifierNames()](reflection.getmodifiernames.md) \- Отримання імен модифікаторів
