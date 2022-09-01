---
navigation:
  - function.forward-static-call-array.html: « forwardstaticcallarray
  - function.func-get-arg.html: funcgetarg »
  - index.html: PHP Manual
  - ref.funchand.html: Функции управления функциями
title: forwardstaticcall
---
# forwardstaticcall

(PHP 5> = 5.3.0, PHP 7, PHP 8)

forwardstaticcall — Виклик статичного методу

### Опис

```methodsynopsis
forward_static_call(callable $callback, mixed ...$args): mixed
```

Виклик функції або методу, задані у параметрі `callback` із наступними аргументами. Ця функція повинна викликатись у контексті методу і не може бути викликана поза класом. Вона використовує [пізніше статичне зв'язування](language.oop5.late-static-bindings.html)

### Список параметрів

`callback`

Функція або метод дзвінка. Цей параметр може бути масивом з ім'ям класу та методу або рядком з ім'ям функції.

`args`

Нуль або більше параметрів, які будуть передані функції, що викликається.

### Значення, що повертаються

Повертає результат функції або **`false`**, у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **forwardstaticcall()****

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
        forward_static_call(array('A', 'test'), 'more', 'args');
        forward_static_call( 'test', 'other', 'args');
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

-   [forwardstaticcallarray()](function.forward-static-call-array.html) - Виклик статичного методу та передача параметрів у вигляді масиву
-   [calluserfuncarray()](function.call-user-func-array.html) - Викликає callback-функцію з масивом параметрів
-   [calluserfunc()](function.call-user-func.html) - Викликає callback-функцію, задану у першому параметрі
-   [ісcallable()](function.is-callable.html) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
