---
navigation:
  - function.create-function.md: « create\_function
  - function.forward-static-call.md: forward\_static\_call »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: forward\_static\_call\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# forward\_static\_call\_array

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

forward\_static\_call\_array — Виклик статичного методу та передача параметрів у вигляді масиву

### Опис

```methodsynopsis
forward_static_call_array(callable $callback, array $args): mixed
```

Викликає функцію користувача або метод, задані в параметрі `callback`. Ця функція повинна викликатись у контексті методу і не може бути викликана поза класом. Вона використовує [пізніше статичне зв'язування](language.oop5.late-static-bindings.md). Усі аргументи пересилаються в метод за значенням та у вигляді масиву, аналогічно [call\_user\_func\_array()](function.call-user-func-array.md)

### Список параметрів

`callback`

Функція або метод дзвінка. Цей параметр може бути масивом з ім'ям класу та методу або рядком з ім'ям функції.

`parameter`

Масив, що містить усі аргументи виклику функції.

> **Зауваження** :
> 
> Пам'ятайте, що аргументи **forward\_static\_call\_array()** не передаються за посиланням.

### Значення, що повертаються

Повертає результат функції або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** forward\_static\_call\_array()\*\*\*\*

```php
<?php

class A
{
    const NAME = 'A';
    public static function test() {
        $args = func_get_args();
        echo static::NAME, " ".join(',', $args)." \n";
    }
}

class B extends A
{
    const NAME = 'B';

    public static function test() {
        echo self::NAME, "\n";
        forward_static_call_array(array('A', 'test'), array('more', 'args'));
        forward_static_call_array( 'test', array('other', 'args'));
    }
}

B::test('foo');

function test() {
        $args = func_get_args();
        echo "C ".join(',', $args)." \n";
    }

?>
```

Результат виконання наведеного прикладу:

```
B
B more,args
C other,args
```

### Дивіться також

-   [forward\_static\_call()](function.forward-static-call.md) \- Виклик статичного методу
-   [call\_user\_func()](function.call-user-func.md) \- Викликає callback-функцію, задану у першому параметрі
-   [call\_user\_func\_array()](function.call-user-func-array.md) \- Викликає callback-функцію з масивом параметрів
-   [is\_callable()](function.is-callable.md) \- Перевіряє, що значення може бути викликане як функція у поточній області видимості
