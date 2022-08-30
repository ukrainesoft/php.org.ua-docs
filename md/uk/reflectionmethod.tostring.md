Повертає рядкову виставу об'єкта ReflectionMethod

-   [« ReflectionMethod::setAccessible](reflectionmethod.setaccessible.html)
    
-   [ReflectionNamedType »](class.reflectionnamedtype.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionMethod](class.reflectionmethod.html)
    
-   Повертає рядкову виставу об'єкта ReflectionMethod
    

# ReflectionMethod::toString

(PHP 5, PHP 7, PHP 8)

ReflectionMethod::toString — Повертає строкове представлення об'єкта ReflectionMethod

### Опис

```methodsynopsis
public ReflectionMethod::__toString(): string
```

Повертає рядкову виставу об'єкта ReflectionMethod.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Строкове представлення об'єкта [ReflectionMethod](class.reflectionmethod.html)

### Приклади

**Приклад #1 Приклад використання **ReflectionMethod::toString()****

```php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod(new HelloWorld(), 'sayHelloTo');
echo $reflectionMethod;
?>
```

Результат виконання цього прикладу:

```
Method [ <user> public method sayHelloTo ] {
  @@ /var/www/examples/reflection.php 16 - 18

  - Parameters [1] {
    Parameter #0 [ <required> $name ]
  }
}
```

### Дивіться також

-   [ReflectionMethod::export()](reflectionmethod.export.html) - Експорт відбитого методу
-   [toString()](language.oop5.magic.html#object.tostring)