Виклик

-   [« ReflectionMethod::getPrototype](reflectionmethod.getprototype.html)
    
-   [ReflectionMethod::invokeArgs »](reflectionmethod.invokeargs.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionMethod](class.reflectionmethod.html)
    
-   Виклик
    

# ReflectionMethod::invoke

(PHP 5, PHP 7, PHP 8)

ReflectionMethod::invoke — Виклик

### Опис

```methodsynopsis
public ReflectionMethod::invoke(?object $object, mixed ...$args): mixed
```

Викликає відбитий метод.

### Список параметрів

`object`

Об'єкт, метод якого потрібно викликати. Для статичних методів передається null.

`args`

Нуль або більше аргументів, що передаються методом. Допускається передавати змінну кількість аргументів.

### Значення, що повертаються

Повертає результат виконання методу.

### Помилки

Викидає виняток [ReflectionException](class.reflectionexception.html), якщо в об'єкті `object` немає визначення методу.

Викидає виняток [ReflectionException](class.reflectionexception.html), якщо викликати метод виконання не вдалося.

### Приклади

**Приклад #1 Приклад використання **ReflectionMethod::invoke()****

```php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
echo $reflectionMethod->invoke(new HelloWorld(), 'Майк');
?>
```

Результат виконання цього прикладу:

```
Привет, Майк
```

### Примітки

> **Зауваження**
> 
> **ReflectionMethod::invoke()** не можна використовувати, якщо очікуються параметри посилання. Замість нього слід використовувати [ReflectionMethod::invokeArgs()](reflectionmethod.invokeargs.html) (Передача посилань у списку аргументів).

### Дивіться також

-   [ReflectionMethod::invokeArgs()](reflectionmethod.invokeargs.html) - виклик методу з передачею аргументів масивом
-   [invoke()](language.oop5.magic.html#object.invoke)
-   [calluserfunc()](function.call-user-func.html) - Викликає callback-функцію, задану у першому параметрі