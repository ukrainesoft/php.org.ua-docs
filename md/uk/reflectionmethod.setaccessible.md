Робить метод доступним

-   [« ReflectionMethod::isStatic](reflectionmethod.isstatic.html)
    
-   [ReflectionMethod::toString »](reflectionmethod.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionMethod](class.reflectionmethod.html)
    
-   Робить метод доступним
    

# ReflectionMethod::setAccessible

(PHP 5> = 5.3.2, PHP 7, PHP 8)

ReflectionMethod::setAccessible — Робить метод доступним

### Опис

```methodsynopsis
public ReflectionMethod::setAccessible(bool $accessible): void
```

Забезпечує доступ до захищеної або закритої властивості за допомогою методу [ReflectionMethod::invoke()](reflectionmethod.invoke.html)

> **Зауваження**: Починаючи з PHP 8.1.0, виклик методу не має сенсу; всі методи викликаються за умовчанням.

### Список параметрів

`accessible`

**`true`**, щоб зробити метод доступним, або **`false`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Визначення простого класу**

```php
<?php
class MyClass
{
    private function foo()
    {
        return 'bar';
    }
}

$method = new ReflectionMethod("MyClass", "foo");
$method->setAccessible(true);

$obj = new MyClass();
echo $method->invoke($obj);
echo $obj->foo();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bar
Fatal error: Uncaught Error: Call to private method MyClass::foo() from global scope in /in/qdaZS:16
```

### Дивіться також

-   [ReflectionMethod::isPrivate()](reflectionmethod.isprivate.html) - Перевіряє, чи є метод закритим
-   [ReflectionMethod::isProtected()](reflectionmethod.isprotected.html) - Перевіряє, чи є метод захищеним