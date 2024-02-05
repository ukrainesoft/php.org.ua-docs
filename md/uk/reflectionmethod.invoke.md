---
navigation:
  - reflectionmethod.hasprototype.md: '« ReflectionMethod::hasPrototype'
  - reflectionmethod.invokeargs.md: 'ReflectionMethod::invokeArgs »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::invoke'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Викидає виняток [ReflectionException](class.reflectionexception.md), якщо в об'єкті `object`нет определения метода.

Викидає виняток [ReflectionException](class.reflectionexception.md), якщо викликати метод виконання не вдалося.

### Приклади

**Пример #1 Пример использования**ReflectionMethod::invoke()\*\*\*\*

```php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Привет, ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
echo $reflectionMethod->invoke(new HelloWorld(), 'Майк');
?>
```

Результат виконання наведеного прикладу:

```
Привет, Майк
```

### Примітки

> **Зауваження** :
> 
> **ReflectionMethod::invoke()** не можна використовувати, якщо очікуються параметри посилання. Замість нього слід використовувати [ReflectionMethod::invokeArgs()](reflectionmethod.invokeargs.md) (Передача посилань у списку аргументів).

### Дивіться також

-   [ReflectionMethod::invokeArgs()](reflectionmethod.invokeargs.md) \- виклик методу з передачею аргументів масивом
-   [\_\_invoke()](language.oop5.magic.md#object.invoke)
-   [call\_user\_func()](function.call-user-func.md) \- Викликає callback-функцію, задану у першому параметрі
