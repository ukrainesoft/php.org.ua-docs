---
navigation:
  - reflectionmethod.invoke.md: '« ReflectionMethod::invoke'
  - reflectionmethod.isabstract.md: 'ReflectionMethod::isAbstract »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::invokeArgs'
---
# ReflectionMethod::invokeArgs

(PHP 5> = 5.1.2, PHP 7, PHP 8)

ReflectionMethod::invokeArgs - Виклик методу з передачею аргументів масивом

### Опис

```methodsynopsis
public ReflectionMethod::invokeArgs(?object $object, array $args): mixed
```

Викликає відбитий спосіб і передає йому аргументи як масиву.

### Список параметрів

`object`

Об'єкт, метод якого викликається. Якщо статичний метод, можна передати null.

`args`

Масив (array), що містить аргументи функції.

### Значення, що повертаються

Повертає результат виконання методу.

### Помилки

Викидає виняток [ReflectionException](class.reflectionexception.md), якщо в об'єкті `object` немає визначення цього.

Викидає виняток [ReflectionException](class.reflectionexception.md), якщо викликати метод виконання не вдалося.

### Приклади

**Приклад #1 Приклад використання **ReflectionMethod::invokeArgs()****

```php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
echo $reflectionMethod->invokeArgs(new HelloWorld(), array('Майк'));
?>
```

Результат виконання цього прикладу:

```
Привет, Майк
```

### Примітки

> **Зауваження**
> 
> Якщо функція має аргументи, які мають бути посиланнями, то вони мають бути посиланнями та в переданому спиці аргументів.

### Дивіться також

-   [ReflectionMethod::invoke()](reflectionmethod.invoke.md) - Виклик
-   [invoke()](language.oop5.magic.html#object.invoke)
-   [calluserfuncarray()](function.call-user-func-array.md) - Викликає callback-функцію з масивом параметрів
