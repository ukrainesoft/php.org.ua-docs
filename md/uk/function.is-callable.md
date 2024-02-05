---
navigation:
  - function.is-bool.md: « is\_bool
  - function.is-countable.md: is\_countable »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: is\_callable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_callable

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

is\_callable — Перевіряє, що значення може бути викликане як функція у поточній області видимості

### Опис

```methodsynopsis
is_callable(mixed $value, bool $syntax_only = false, string &$callable_name = null): bool
```

Перевіряє, що значення є [callable](language.types.callable.md)

### Список параметрів

`value`

Значення для перевірки

`syntax_only`

Якщо дорівнює **`true`**, функція тільки перевіряє, що `value` може бути функцією чи методом. У цьому випадку відхилятимуться змінні, які не є ні рядком, ні масивом з коректною структурою для використання як callback-функції. Коректна структура масиву передбачає наявність лише двох елементів, перший у тому числі - об'єкт чи рядок, а другий - лише рядок.

`callable_name`

Отримує ім'я, що викликається. У прикладі нижче це "someClass:: someMethod". Слід пам'ятати, що хоча запис someClass::SomeMethod() означає статичний метод, що викликається, це не так.

### Значення, що повертаються

Повертає **`true`**, якщо `value` може бути викликана, або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** is\_callable()\*\*\*\*

```php
<?php
//  Как проверить переменную, чтобы узнать, может ли она быть вызвана
//  как функция.

//
//  Простая переменная, содержащая имя функции
//

function someFunction()
{
}

$functionVariable = 'someFunction';

var_dump(is_callable($functionVariable, false, $callable_name));  // bool(true)

echo $callable_name, "\n";  // someFunction

//
//  Массив, содержащий метод класса
//

class someClass {

  function someMethod()
  {
  }

}

$anObject = new someClass();

$methodVariable = array($anObject, 'someMethod');

var_dump(is_callable($methodVariable, true, $callable_name));  //  bool(true)

echo $callable_name, "\n";  //  someClass::someMethod

?>
```

**Приклад #2**is\_callable()\*\* та конструктори\*\*

Функция**is\_callable()** не рахує конструктори за callable.

```php
<?php

class Foo
{
    public function __construct() {}
    public function foo() {}
}

var_dump(
    is_callable(array('Foo', '__construct')),
    is_callable(array('Foo', 'foo'))
);
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
```

### Примітки

-   Об'єкт завжди є callable, якщо він реалізує[\_\_invoke()](language.oop5.magic.md#object.invoke), і цей метод доступний у поточній області видимості.
-   Ім'я класу є callable, якщо воно реалізує[\_\_callStatic()](language.oop5.overloading.md#object.callstatic)
-   Якщо об'єкт реалізує[\_\_call()](language.oop5.overloading.md#object.call)тоді ця функція поверне\*\*`true`\*\*для будь-якого методу цього об'єкта, навіть якщо метод не визначено.
-   Функція може запускати автозавантаження, якщо викликається під назвою класу.

### Дивіться також

-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
-   [method\_exists()](function.method-exists.md) \- Перевіряє, чи існує метод у даному класі
