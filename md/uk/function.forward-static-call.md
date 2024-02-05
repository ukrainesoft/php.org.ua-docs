---
navigation:
  - function.forward-static-call-array.md: « forward\_static\_call\_array
  - function.func-get-arg.md: func\_get\_arg »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: forward\_static\_call
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# forward\_static\_call

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

forward\_static\_call — Виклик статичного методу

### Опис

```methodsynopsis
forward_static_call(callable $callback, mixed ...$args): mixed
```

Виклик функції або методу, задані у параметрі `callback` із наступними аргументами. Ця функція повинна викликатись у контексті методу і не може бути викликана поза класом. Вона використовує [пізніше статичне зв'язування](language.oop5.late-static-bindings.md)

### Список параметрів

`callback`

Функція або метод дзвінка. Цей параметр може бути масивом з ім'ям класу та методу або рядком з ім'ям функції.

`args`

Нуль або більше параметрів, які будуть передані функції, що викликається.

### Значення, що повертаються

Повертає результат функції або **`false`**, у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**forward\_static\_call()\*\*\*\*

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
        forward_static_call(array('A', 'test'), 'more', 'args');
        forward_static_call( 'test', 'other', 'args');
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

-   [forward\_static\_call\_array()](function.forward-static-call-array.md) \- Виклик статичного методу та передача параметрів у вигляді масиву
-   [call\_user\_func\_array()](function.call-user-func-array.md) \- Викликає callback-функцію з масивом параметрів
-   [call\_user\_func()](function.call-user-func.md) \- Викликає callback-функцію, задану у першому параметрі
-   [is\_callable()](function.is-callable.md) \- Перевіряє, що значення може бути викликане як функція у поточній області видимості
