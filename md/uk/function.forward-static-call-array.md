Виклик статичного методу та передача параметрів у вигляді масиву

-   [« createfunction](function.create-function.html)
    
-   [forwardstaticcall »](function.forward-static-call.html)
    
-   [PHP Manual](index.html)
    
-   [Функции управления функциями](ref.funchand.html)
    
-   Виклик статичного методу та передача параметрів у вигляді масиву
    

# forwardstaticcallarray

(PHP 5> = 5.3.0, PHP 7, PHP 8)

forwardstaticcallarray — Виклик статичного методу та передача параметрів у вигляді масиву

### Опис

```methodsynopsis
forward_static_call_array(callable $callback, array $args): mixed
```

Викликає функцію користувача або метод, задані в параметрі `callback`. Ця функція повинна викликатись у контексті методу і не може бути викликана поза класом. Вона використовує [пізніше статичне зв'язування](language.oop5.late-static-bindings.html). Усі аргументи пересилаються в метод за значенням та у вигляді масиву, аналогічно [calluserfuncarray()](function.call-user-func-array.html)

### Список параметрів

`callback`

Функція або метод дзвінка. Цей параметр може бути масивом з ім'ям класу та методу або рядком з ім'ям функції.

`parameter`

Масив, що містить усі аргументи виклику функції.

> **Зауваження**
> 
> Пам'ятайте, що аргументи **forwardstaticcallarray()** не передаються за посиланням.

### Значення, що повертаються

Повертає результат функції або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **forwardstaticcallarray()****

```php
<?php

class A
{
    const NAME = 'A';
    public static function test() {
        $args = func_get_args();
        echo static::NAME, " ".join(',', $args)." \n";
    }
}

class B extends A
{
    const NAME = 'B';

    public static function test() {
        echo self::NAME, "\n";
        forward_static_call_array(array('A', 'test'), array('more', 'args'));
        forward_static_call_array( 'test', array('other', 'args'));
    }
}

B::test('foo');

function test() {
        $args = func_get_args();
        echo "C ".join(',', $args)." \n";
    }

?>
```

Результат виконання цього прикладу:

```
B
B more,args
C other,args
```

### Дивіться також

-   [forwardstaticcall()](function.forward-static-call.html) - Виклик статичного методу
-   [calluserfunc()](function.call-user-func.html) - Викликає callback-функцію, задану у першому параметрі
-   [calluserfuncarray()](function.call-user-func-array.html) - Викликає callback-функцію з масивом параметрів
-   [ісcallable()](function.is-callable.html) - Перевіряє, що значення може бути викликане як функція у поточній області видимості