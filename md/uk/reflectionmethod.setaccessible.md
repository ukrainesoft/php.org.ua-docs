---
navigation:
  - reflectionmethod.ispublic.md: '« ReflectionMethod::isPublic'
  - reflectionmethod.tostring.md: 'ReflectionMethod::\_\_toString »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::setAccessible'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::setAccessible

(PHP 5 >= 5.3.2, PHP 7, PHP 8)

ReflectionMethod::setAccessible — Робить метод доступним

### Опис

```methodsynopsis
public ReflectionMethod::setAccessible(bool $accessible): void
```

Забезпечує доступ до захищеної або закритої властивості за допомогою методу [ReflectionMethod::invoke()](reflectionmethod.invoke.md)

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
class MyClass
{
    private function foo()
    {
        return 'bar';
    }
}

$method = new ReflectionMethod("MyClass", "foo");
$method->setAccessible(true);

$obj = new MyClass();
echo $method->invoke($obj);
echo $obj->foo();
?>
```

Висновок наведеного прикладу буде схожим на:

```
bar
Fatal error: Uncaught Error: Call to private method MyClass::foo() from global scope in /in/qdaZS:16
```

### Дивіться також

-   [ReflectionMethod::isPrivate()](reflectionmethod.isprivate.md) \- Перевіряє, чи є метод закритим
-   [ReflectionMethod::isProtected()](reflectionmethod.isprotected.md) \- Перевіряє, чи є метод захищеним
