---
navigation:
  - ref.funchand.md: « Функции управления функциями
  - function.call-user-func.md: calluserfunc »
  - index.md: PHP Manual
  - ref.funchand.md: Функции управления функциями
title: calluserfuncarray
---
# calluserfuncarray

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

calluserfuncarray - Викликає callback-функцію з масивом параметрів

### Опис

```methodsynopsis
call_user_func_array(callable $callback, array $args): mixed
```

Викликає callback-функцію `callback`, з параметрами з масиву `args`

### Список параметрів

`callback`

Функція типу, що викликається [callable](language.types.callable.md)

`args`

Параметри, що передаються в функцію, у вигляді індексованого масиву.

### Значення, що повертаються

Повертає результат функції або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Ключі параметра `args` тепер інтерпретуються як імена параметрів, а чи не ігноруються. |

### Приклади

**Приклад #1 Приклад використання функції **calluserfuncarray()****

```php
<?php
function foobar($arg, $arg2) {
    echo __FUNCTION__, " got $arg and $arg2\n";
}
class foo {
    function bar($arg, $arg2) {
        echo __METHOD__, " got $arg and $arg2\n";
    }
}


// Вызываем функцию foobar() с 2 аргументами
call_user_func_array("foobar", array("one", "two"));

// Вызываем метод $foo->bar() с 2 аргументами
$foo = new foo;
call_user_func_array(array($foo, "bar"), array("three", "four"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
foobar got one and two
foo::bar got three and four
```

**Приклад #2 Приклад використання **calluserfuncarray()** з ім'ям простору імен**

```php
<?php

namespace Foobar;

class Foo {
    static public function test($name) {
        print "Hello {$name}!\n";
    }
}

call_user_func_array(__NAMESPACE__ .'\Foo::test', array('Hannes'));

call_user_func_array(array(__NAMESPACE__ .'\Foo', 'test'), array('Philip'));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Hello Hannes!
Hello Philip!
```

**Приклад #3 Використання лямбда-функції**

```php
<?php

$func = function($arg1, $arg2) {
    return $arg1 * $arg2;
};

var_dump(call_user_func_array($func, array(2, 4)));

?>
```

Результат виконання цього прикладу:

```
int(8)
```

**Приклад #4 Передача значень за посиланням**

```php
<?php

function mega(&$a){
    $a = 55;
    echo "function mega \$a=$a\n";
}
$bar = 77;
call_user_func_array('mega',array(&$bar));
echo "global \$bar=$bar\n";

?>
```

Результат виконання цього прикладу:

```
function mega $a=55
global $bar=55
```

### Примітки

> **Зауваження**
> 
> Callback-функції, зареєстровані такими функціями як [calluserfunc()](function.call-user-func.md) і **calluserfuncarray()**, не будуть викликані за наявності не спійманого виключення, кинутого у попередній callback-функції.

### Дивіться також

-   [calluserfunc()](function.call-user-func.md) - Викликає callback-функцію, задану у першому параметрі
-   [ReflectionFunction::invokeArgs()](reflectionfunction.invokeargs.md) - Виклик функції із передачею аргументів
-   [ReflectionMethod::invokeArgs()](reflectionmethod.invokeargs.md) - виклик методу з передачею аргументів масивом
