Перевіряє, чи заданий метод

-   [« ReflectionClass::hasConstant](reflectionclass.hasconstant.md)
    
-   [ReflectionClass::hasProperty »](reflectionclass.hasproperty.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionClass](class.reflectionclass.md)
    
-   Перевіряє, чи заданий метод
    

# ReflectionClass::hasMethod

(PHP 5> = 5.1.2, PHP 7, PHP 8)

ReflectionClass::hasMethod — Перевіряє, чи заданий метод

### Опис

```methodsynopsis
public ReflectionClass::hasMethod(string $name): bool
```

Перевіряє, чи в класі визначений зазначений метод чи ні.

### Список параметрів

`name`

Ім'я методу, що перевіряється.

### Значення, що повертаються

**`true`**, якщо метод визначено, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::hasMethod()****

```php
<?php
Class C {
    public function publicFoo() {
        return true;
    }

    protected function protectedFoo() {
        return true;
    }

    private function privateFoo() {
        return true;
    }

    static function staticFoo() {
        return true;
    }
}

$rc = new ReflectionClass("C");

var_dump($rc->hasMethod('publicFoo'));

var_dump($rc->hasMethod('protectedFoo'));

var_dump($rc->hasMethod('privateFoo'));

var_dump($rc->hasMethod('staticFoo'));

// C не имеет метода bar
var_dump($rc->hasMethod('bar'));

// Имена методов регистронезависимые
var_dump($rc->hasMethod('PUBLICfOO'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionClass::hasConstant()](reflectionclass.hasconstant.md) - Перевіряє, чи визначено константу
-   [ReflectionClass::hasProperty()](reflectionclass.hasproperty.md) - Перевіряє, чи визначено властивість