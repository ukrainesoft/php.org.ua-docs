Повертає екземпляр ReflectionMethod для методу класу

-   [« ReflectionClass::getInterfaces](reflectionclass.getinterfaces.html)
    
-   [ReflectionClass::getMethods »](reflectionclass.getmethods.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Повертає екземпляр ReflectionMethod для методу класу
    

# ReflectionClass::getMethod

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getMethod — Повертає екземпляр [ReflectionMethod](class.reflectionmethod.html) для методу класу

### Опис

```methodsynopsis
public ReflectionClass::getMethod(string $name): ReflectionMethod
```

Повертає екземпляр [ReflectionMethod](class.reflectionmethod.html) для методу класу

### Список параметрів

`name`

Досліджуваний метод.

### Значення, що повертаються

Екземпляр класу [ReflectionMethod](class.reflectionmethod.html)

### Помилки

[ReflectionException](class.reflectionexception.html) якщо метод не існує.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getMethod()****

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$method = $class->getMethod('getMethod');
var_dump($method);
?>
```

Результат виконання цього прикладу:

```
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(9) "getMethod"
  ["class"]=>
  string(15) "ReflectionClass"
}
```

### Дивіться також

-   [ReflectionClass::getMethods()](reflectionclass.getmethods.html) - Повертає список методів у вигляді масиву