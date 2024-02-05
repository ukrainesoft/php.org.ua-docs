---
navigation:
  - function.call-user-func-array.md: « call\_user\_func\_array
  - function.create-function.md: create\_function »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: call\_user\_func
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# call\_user\_func

(PHP 4, PHP 5, PHP 7, PHP 8)

call\_user\_func — Викликає callback-функцію, задану у першому параметрі

### Опис

```methodsynopsis
call_user_func(callable $callback, mixed ...$args): mixed
```

Викликає callback-функцію, передану першим параметром, і передає інші параметри як аргументи . `callback`

### Список параметрів

`callback`

Функція типу, що викликається [callable](language.types.callable.md)

`args`

Нуль або більше параметрів, що передаються в callback-функцію.

> **Зауваження** :
> 
> Врахуйте, що параметри для **call\_user\_func()** не передаються за посиланням.
> 
> **Приклад #1 Приклад використання** call\_user\_func()\*\* та посилання\*\*
> 
> ```php
> <?php
> error_reporting(E_ALL);
> function increment(&$var)
> {
>     $var++;
> }
> 
> $a = 0;
> call_user_func('increment', $a);
> echo $a."\n";
> 
> // Натомість можна використовувати цей спосіб
> call_user_func_array('increment', array(&$a));
> echo $a."\n";
> 
> // Також можна використовувати функцію як змінну
> $increment = 'increment';
> $increment($a);
> echo $a."\n";
> ?>
> ```
> 
> Результат виконання наведеного прикладу:
> 
> ```
> Warning: Parameter 1 to increment() expected to be a reference, value given in …
> 0
> 1
> 2
> ```

### Значення, що повертаються

Повертає значення, повернене callback-функцією.

### Приклади

**Приклад #2 Приклад використання** call\_user\_func()\*\*\*\*

```php
<?php
function barber($type)
{
    echo "Вы хотели стрижку $type, без проблем\n";
}
call_user_func('barber', "под горшок");
call_user_func('barber', "наголо");
?>
```

Результат виконання наведеного прикладу:

```
Вы хотели стрижку под горшок, без проблем
Вы хотели стрижку наголо, без проблем
```

**Приклад #3 Использование**call\_user\_func()**, використовуючи простір імен**

```php
<?php

namespace Foobar;

class Foo {
    static public function test() {
        print "Привет, мир!\n";
    }
}

call_user_func(__NAMESPACE__ .'\Foo::test');
call_user_func(array(__NAMESPACE__ .'\Foo', 'test'));

?>
```

Результат виконання наведеного прикладу:

```
Привет, мир!
Привет, мир!
```

**Приклад #4 Виклик методу класу за допомогою **call\_user\_func()****

```php
<?php

class myclass {
    static function say_hello()
    {
        echo "Привет!\n";
    }
}

$classname = "myclass";

call_user_func(array($classname, 'say_hello'));
call_user_func($classname .'::say_hello');

$myobject = new myclass();

call_user_func(array($myobject, 'say_hello'));

?>
```

Результат виконання наведеного прикладу:

```
Привет!
Привет!
Привет!
```

**Приклад #5 Использование лямбда-функции с**call\_user\_func()\*\*\*\*

```php
<?php
call_user_func(function($arg) { print "[$arg]\n"; }, 'test');
?>
```

Результат виконання наведеного прикладу:

```
[test]
```

### Примітки

> **Зауваження** :
> 
> Callback-функції, зареєстровані такими функціями як \*\*call\_user\_func()\*\*и[call\_user\_func\_array()](function.call-user-func-array.md), не будуть викликані за наявності не спійманого виключення, кинутого у попередній callback-функції.

### Дивіться також

-   [call\_user\_func\_array()](function.call-user-func-array.md) \- Викликає callback-функцію з масивом параметрів
-   [is\_callable()](function.is-callable.md) \- Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [Звернення до функцій через змінні](functions.variable-functions.md)
-   [ReflectionFunction::invoke()](reflectionfunction.invoke.md) \- Викликає функцію
-   [ReflectionMethod::invoke()](reflectionmethod.invoke.md) \- Виклик
