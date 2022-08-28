Викликає callback-функцію, задану у першому параметрі

-   [« call\_user\_func\_array](function.call-user-func-array.html)
    
-   [create\_function »](function.create-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции управления функциями](ref.funchand.html)
    
-   Викликає callback-функцію, задану у першому параметрі
    

# calluserfunc

(PHP 4, PHP 5, PHP 7, PHP 8)

calluserfunc — Викликає callback-функцію, задану у першому параметрі

### Опис

```methodsynopsis
call_user_func(callable $callback, mixed ...$args): mixed
```

Викликає callback-функцію, передану першим параметром, і передає інші параметри як аргументи . `callback`

### Список параметрів

`callback`

Функція типу, що викликається [callable](language.types.callable.html)

`args`

Нуль або більше параметрів, що передаються в callback-функцію.

> **Зауваження**
> 
> Врахуйте, що параметри для **calluserfunc()** не передаються за посиланням.
> 
> **Приклад #1 Приклад використання **calluserfunc()** та посилання**
> 
> ```php
> <?php
> error_reporting(E_ALL);
> function increment(&$var)
> {
>     $var++;
> }
> 
> $a = 0;
> call_user_func('increment', $a);
> echo $a."\n";
> 
> // Вместо этого можно использовать этот способ
> call_user_func_array('increment', array(&$a));
> echo $a."\n";
> 
> // Также можно использовать функцию в качестве переменной
> $increment = 'increment';
> $increment($a);
> echo $a."\n";
> ?>
> ```
> 
> Результат виконання цього прикладу:
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

**Приклад #2 Приклад використання **calluserfunc()****

```php
<?php
function barber($type)
{
    echo "Вы хотели стрижку $type, без проблем\n";
}
call_user_func('barber', "под горшок");
call_user_func('barber', "наголо");
?>
```

Результат виконання цього прикладу:

```
Вы хотели стрижку под горшок, без проблем
Вы хотели стрижку наголо, без проблем
```

**Приклад #3 Використання **calluserfunc()**, використовуючи простір імен**

```php
<?php

namespace Foobar;

class Foo {
    static public function test() {
        print "Привет, мир!\n";
    }
}

call_user_func(__NAMESPACE__ .'\Foo::test');
call_user_func(array(__NAMESPACE__ .'\Foo', 'test'));

?>
```

Результат виконання цього прикладу:

```
Привет, мир!
Привет, мир!
```

**Приклад #4 Виклик методу класу за допомогою **calluserfunc()****

```php
<?php

class myclass {
    static function say_hello()
    {
        echo "Привет!\n";
    }
}

$classname = "myclass";

call_user_func(array($classname, 'say_hello'));
call_user_func($classname .'::say_hello');

$myobject = new myclass();

call_user_func(array($myobject, 'say_hello'));

?>
```

Результат виконання цього прикладу:

```
Привет!
Привет!
Привет!
```

**Приклад #5 Використання лямбда-функції з **calluserfunc()****

```php
<?php
call_user_func(function($arg) { print "[$arg]\n"; }, 'test');
?>
```

Результат виконання цього прикладу:

```
[test]
```

### Примітки

> **Зауваження**
> 
> Callback-функції, зареєстровані такими функціями як **calluserfunc()** і [call\_user\_func\_array()](function.call-user-func-array.html), не будуть викликані за наявності не спійманого виключення, кинутого у попередній callback-функції.

### Дивіться також

-   [call\_user\_func\_array()](function.call-user-func-array.html) - Викликає callback-функцію з масивом параметрів
-   [is\_callable()](function.is-callable.html) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [Обращение к функциям через переменные](functions.variable-functions.html)
-   [ReflectionFunction::invoke()](reflectionfunction.invoke.html) - Викликає функцію
-   [ReflectionMethod::invoke()](reflectionmethod.invoke.html) - Виклик