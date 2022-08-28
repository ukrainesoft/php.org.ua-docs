Отримує модифікатори методу

-   [« ReflectionMethod::getDeclaringClass](reflectionmethod.getdeclaringclass.html)
    
-   [ReflectionMethod::getPrototype »](reflectionmethod.getprototype.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionMethod](class.reflectionmethod.html)
    
-   Отримує модифікатори методу
    

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

Числове уявлення модифікаторів. Описи та значення цих модифікаторів наведено у списку [предопределённых констант](class.reflectionmethod.html#reflectionmethod.constants.modifiers)

### Приклади

**Приклад #1 Приклад використання **ReflectionMethod::getModifiers()****

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

echo "Модификаторы метода foo():\n";
echo $foo->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($foo->getModifiers())) . "\n";

$bar = new ReflectionMethod('Testing', 'bar');

echo "Модификаторы метода bar():\n";
echo $bar->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($bar->getModifiers()));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Модификаторы метода foo():
49
final public static
Модификаторы метода bar():
1
public
```

### Дивіться також

-   [Reflection::getModifierNames()](reflection.getmodifiernames.html) - Отримання імен модифікаторів