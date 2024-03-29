---
navigation:
  - reflectionmethod.invoke.md: '« ReflectionMethod::invoke'
  - reflectionmethod.isabstract.md: 'ReflectionMethod::isAbstract »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::invokeArgs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::invokeArgs

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

ReflectionMethod::invokeArgs - Виклик методу з передачею аргументів масивом

### Опис

```methodsynopsis
public ReflectionMethod::invokeArgs(?object $object, array $args): mixed
```

Викликає відбитий спосіб і передає йому аргументи як масиву.

### Список параметрів

`object`

Об’єкт, метод якого викликається. Якщо метод є статичним, ви можете передати значення null.

`args`

Масив, що містить аргументи функції.

### Значення, що повертаються

Повертає результат виконання методу.

### Помилки

Викидає виняток [ReflectionException](class.reflectionexception.md), якщо в об'єкті `object` немає визначення цього.

Викидає виняток [ReflectionException](class.reflectionexception.md), якщо викликати метод виконання не вдалося.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Ключі `args` тепер інтерпретуються як імена параметрів, а чи не ігноруються. |

### Приклади

**Приклад #1 Приклад використання** ReflectionMethod::invokeArgs()\*\*\*\*

```php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
echo $reflectionMethod->invokeArgs(new HelloWorld(), array('Майк'));
?>
```

Результат виконання наведеного прикладу:

```
Привет, Майк
```

### Примітки

> **Зауваження** :
> 
> Якщо функція має аргументи, які мають бути посиланнями, то вони мають бути посиланнями та в переданому спиці аргументів.

### Дивіться також

-   [ReflectionMethod::invoke()](reflectionmethod.invoke.md) \- Виклик
-   [\_\_invoke()](language.oop5.magic.md#object.invoke)
-   [call\_user\_func\_array()](function.call-user-func-array.md) \- Викликає callback-функцію з масивом параметрів
