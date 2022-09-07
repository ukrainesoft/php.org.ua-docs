---
navigation:
  - language.types.null.md: « NULL
  - language.types.declarations.md: Оголошення типів »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Функції зворотного дзвінка (callback-функції)
---
## Функції зворотного дзвінка (callback-функції)

Callback-функції можуть бути позначені оголошенням типу [callable](language.types.callable.md)

Деякі функції, такі як [calluserfunc()](function.call-user-func.md) або [usort()](function.usort.md), приймають певні користувачем callback-функції як параметр. Callback-функції може бути як простими функціями, і методами об'єктів, включаючи статичні методи класів.

### Передача

У PHP функції передаються на ім'я у вигляді рядка. Можна використовувати будь-які вбудовані або створені користувачем функції, за винятком конструкцій мови, таких як: [array()](function.array.md) [echo](function.echo.md) [empty()](function.empty.md) [eval()](function.eval.md) [exit()](function.exit.md) [isset()](function.isset.md) [list()](function.list.md) [print](function.print.md) або [unset()](function.unset.md)

Метод створеного об'єкта (object) передається як масив, що містить об'єкт за індексом 0 та ім'я методу за індексом 1. Доступ до закритих та захищених методів дозволено зсередини класу.

Статичні методи класу також можуть бути викликані без створення екземпляра об'єкта класу шляхом передачі імені класу замість об'єкта в елементі масиву з індексом 0 або виконання `'ClassName::methodName'`

Крім звичайних функцій користувача, в якості callback-функції можна передавати [анонімні функції](functions.anonymous.md) і [стрілочні функції](functions.arrow.md)

> **Зауваження**
> 
> Починаючи з PHP 8.1.0, у [Callback-функцій як об'єктів першого класу](functions.first_class_callable_syntax.md) та сама семантика, що й у цього методу.

Як правило, будь-який об'єкт, що реалізує [invoke()](language.oop5.magic.md#object.invoke), також може бути передано до параметра callback.

**Приклад #1 Приклад callback-функції**

```php
<?php

// Пример callback-функции
function my_callback_function() {
    echo 'Привет, мир!';
}

// Пример callback-метода
class MyClass {
    static function myCallbackMethod() {
        echo 'Привет, мир!';
    }
}

// Тип 1: Простой callback
call_user_func('my_callback_function');

// Тип 2: Вызов статического метода класса
call_user_func(array('MyClass', 'myCallbackMethod'));

// Тип 3: Вызов метода класса
$obj = new MyClass();
call_user_func(array($obj, 'myCallbackMethod'));

// Тип 4: Вызов статического метода класса
call_user_func('MyClass::myCallbackMethod');

// Тип 5: Вызов относительного статического метода
class A {
    public static function who() {
        echo "A\n";
    }
}

class B extends A {
    public static function who() {
        echo "B\n";
    }
}

call_user_func(array('B', 'parent::who')); // A

// Тип 6: Объекты, реализующие __invoke, могут быть использованы как callback
class C {
    public function __invoke($name) {
        echo 'Привет ', $name, "\n";
    }
}

$c = new C();
call_user_func($c, 'PHP!');
?>
```

**Приклад #2 Приклад callback-функції з використанням замикання**

```php
<?php
// Наше замыкание
$double = function($a) {
    return $a * 2;
};

// Диапазон чисел
$numbers = range(1, 5);

// Использование замыкания в качестве callback-функции
// для удвоения каждого элемента в нашем диапазоне
$new_numbers = array_map($double, $numbers);

print implode(' ', $new_numbers);
?>
```

Результат виконання цього прикладу:

```
2 4 6 8 10
```

> **Зауваження**
> 
> Callback-функції, зареєстровані такими функціями як [calluserfunc()](function.call-user-func.md) і [calluserfuncarray()](function.call-user-func-array.md), не будуть викликані за наявності не спійманого виключення, кинутого у попередній callback-функції.
