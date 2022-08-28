Отримання класу, що оголошує

-   [« ReflectionParameter::getClass](reflectionparameter.getclass.html)
    
-   [ReflectionParameter::getDeclaringFunction »](reflectionparameter.getdeclaringfunction.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionParameter](class.reflectionparameter.html)
    
-   Отримання класу, що оголошує
    

# ReflectionParameter::getDeclaringClass

(PHP 5> = 5.1.3, PHP 7, PHP 8)

ReflectionParameter::getDeclaringClass — Отримання класу, що оголошує

### Опис

```methodsynopsis
public ReflectionParameter::getDeclaringClass(): ?ReflectionClass
```

Отримує клас, що оголошує.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт класу [ReflectionClass](class.reflectionclass.html), або **`null`**, якщо викликано для функції.

### Приклади

**Приклад #1 Отримання класу, в якому оголошено метод**

```php
<?php
class Foo
{
    public function bar(\DateTime $datetime)
    {
    }
}

class Baz extends Foo
{
}

$param = new \ReflectionParameter(['Baz', 'bar'], 0);

var_dump($param->getDeclaringClass());
```

Результат виконання цього прикладу:

```
object(ReflectionClass)#2 (1) {
  ["name"]=>
  string(3) "Foo"
}
```

### Дивіться також

-   [ReflectionParameter::getClass()](reflectionparameter.getclass.html) - Отримує об'єкт ReflectionClass для параметра, що відображається, або null