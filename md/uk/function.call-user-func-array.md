---
navigation:
  - ref.funchand.md: « Функції керування функціями
  - function.call-user-func.md: call\_user\_func »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: call\_user\_func\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# call\_user\_func\_array

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

call\_user\_func\_array - Викликає callback-функцію з масивом параметрів

### Опис

```methodsynopsis
call_user_func_array(callable $callback, array $args): mixed
```

Викликає callback-функцію `callback`, з параметрами з масиву `args`

### Список параметрів

`callback`

Функція типу, що викликається [callable](language.types.callable.md)

`args`

Параметри, що передаються в функцію, у вигляді масиву.

Якщо всі ключі `args` є числовими, ключі ігноруються і кожен елемент буде передано до параметра `callback` як позиційний аргумент по порядку.

Якщо якісь ключі `args` є рядками, ці елементи будуть передані до параметра `callback` як іменовані аргументи з ім'ям, заданим ключем.

Відбудеться непоправна помилка, якщо числовий ключ у `args` з'являється після рядкового ключа або якщо рядковий ключ не збігається з ім'ям будь-якого параметра `callback`

### Значення, що повертаються

Повертає результат функції або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Ключі параметра `args` тепер інтерпретуються як імена параметрів, а чи не ігноруються. |

### Приклади

**Приклад #1 Приклад использования функции**call\_user\_func\_array()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
foobar got one and two
foo::bar got three and four
```

**Приклад #2 Приклад використання** call\_user\_func\_array()\*\* з ім'ям простору імен\*\*

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

Висновок наведеного прикладу буде схожим на:

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

Результат виконання наведеного прикладу:

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

Результат виконання наведеного прикладу:

```
function mega $a=55
global $bar=55
```

**Приклад #5 Приклад використання** call\_user\_func\_array()\*\* з іменованими аргументами\*\*

```php
<?php
function foobar($first, $second) {
    echo __FUNCTION__, " получает $first и $second\n";
}

// Вызов функции foobar() с именованными аргументами в непозиционном порядке
call_user_func_array("foobar", array("second" => "two", "first" => "one"));

// Вызов функции foobar() с одним именованным аргументом
call_user_func_array("foobar", array("foo", "second" => "bar"));

// Неисправимая ошибка: Невозможно использовать позиционный аргумент после именованного аргумента
call_user_func_array("foobar", array("first" => "one", "bar"));

?>
```

Висновок наведеного прикладу буде схожим на:

```
foobar получает one и two
foobar получает foo и bar

Fatal error: Uncaught Error: Cannot use positional argument after named argument
```

### Примітки

> **Зауваження** :
> 
> Callback-функції, зареєстровані такими функціями як [call\_user\_func()](function.call-user-func.md)и**call\_user\_func\_array()**, не будуть викликані за наявності не спійманого виключення, кинутого у попередній callback-функції.

### Дивіться також

-   [call\_user\_func()](function.call-user-func.md) \- Викликає callback-функцію, задану у першому параметрі
-   [ReflectionFunction::invokeArgs()](reflectionfunction.invokeargs.md) \- Виклик функції із передачею аргументів
-   [ReflectionMethod::invokeArgs()](reflectionmethod.invokeargs.md) \- виклик методу з передачею аргументів масивом
