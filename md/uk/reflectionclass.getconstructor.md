Повертає конструктор класу

-   [« ReflectionClass::getConstants](reflectionclass.getconstants.html)
    
-   [ReflectionClass::getDefaultProperties »](reflectionclass.getdefaultproperties.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Повертає конструктор класу
    

# ReflectionClass::getConstructor

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getConstructor — Повертає конструктор класу

### Опис

```methodsynopsis
public ReflectionClass::getConstructor(): ?ReflectionMethod
```

Повертає конструктор відбитого класу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт [ReflectionMethod](class.reflectionmethod.html), що відображає конструктор класу, або **`null`** якщо клас не має конструктора.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getConstructor()****

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$constructor = $class->getConstructor();
var_dump($constructor);
?>
```

Результат виконання цього прикладу:

```
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(11) "__construct"
  ["class"]=>
  string(15) "ReflectionClass"
}
```

### Дивіться також

-   [ReflectionClass::getName()](reflectionclass.getname.html) - Повертає ім'я класу