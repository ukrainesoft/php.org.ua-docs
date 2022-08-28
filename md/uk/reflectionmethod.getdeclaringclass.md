Отримує клас, що оголошує відбитий метод

-   [« ReflectionMethod::getClosure](reflectionmethod.getclosure.html)
    
-   [ReflectionMethod::getModifiers »](reflectionmethod.getmodifiers.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionMethod](class.reflectionmethod.html)
    
-   Отримує клас, що оголошує відбитий метод
    

# ReflectionMethod::getDeclaringClass

(PHP 5, PHP 7, PHP 8)

ReflectionMethod::getDeclaringClass — Отримує клас, що оголошує відбитий метод

### Опис

```methodsynopsis
public ReflectionMethod::getDeclaringClass(): ReflectionClass
```

Отримує клас, що оголошує відбитий метод.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт класу [ReflectionClass](class.reflectionclass.html)частиною якого є відбитий метод.

### Приклади

**Приклад #1 Приклад використання **ReflectionMethod::getDeclaringClass()****

```php
<?php
class HelloWorld {

    protected function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod(new HelloWorld(), 'sayHelloTo');
var_dump($reflectionMethod->getDeclaringClass());
?>
```

Результат виконання цього прикладу:

```
object(ReflectionClass)#2 (1) {
  ["name"]=>
  string(10) "HelloWorld"
}
```

### Дивіться також

-   [ReflectionMethod::isAbstract()](reflectionmethod.isabstract.html) - Перевіряє, чи є метод абстрактним