---
navigation:
  - language.operators.array.md: '« Оператори, які працюють з масивами'
  - language.control-structures.html: Управляющие конструкции »
  - index.md: PHP Manual
  - language.operators.md: Оператори
title: Оператор перевірки типу
---
## Оператор перевірки типу

Оператор `instanceof` використовується для визначення того, чи є поточний об'єкт примірником зазначеного [класса](language.oop5.basic.html#language.oop5.basic.class)

**Приклад #1 Використання `instanceof` з класами**

```php
<?php
class MyClass
{
}

class NotMyClass
{
}
$a = new MyClass;

var_dump($a instanceof MyClass);
var_dump($a instanceof NotMyClass);
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

Оператор `instanceof` також може бути використаний для визначення, чи успадковує певний об'єкт будь-який клас:

**Приклад #2 Використання `instanceof` з успадкованими класами**

```php
<?php
class ParentClass
{
}

class MyClass extends ParentClass
{
}

$a = new MyClass;

var_dump($a instanceof MyClass);
var_dump($a instanceof ParentClass);
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
```

Для перевірки *неприладдя* об'єкта деякому класу, використовуйте [логічний оператор`not`](language.operators.logical.md)

**Приклад #3 Використання `instanceof` для перевірки того, що об'єкт *не* є екземпляром класу**

```php
<?php
class MyClass
{
}

$a = new MyClass;
var_dump(!($a instanceof stdClass));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

Зрештою, `instanceof` може бути також використаний для перевірки реалізації об'єктом деякого [інтерфейсу](language.oop5.interfaces.md)

**Приклад #4 Використання `instanceof` з інтерфейсами**

```php
<?php
interface MyInterface
{
}

class MyClass implements MyInterface
{
}

$a = new MyClass;

var_dump($a instanceof MyClass);
var_dump($a instanceof MyInterface);
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
```

Хоча `instanceof` зазвичай використовується з прямо вказаним ім'ям класу, він також може бути використаний з іншим об'єктом або рядковою змінною:

**Приклад #5 Використання `instanceof` з іншими змінними**

```php
<?php
interface MyInterface
{
}

class MyClass implements MyInterface
{
}

$a = new MyClass;
$b = new MyClass;
$c = 'MyClass';
$d = 'NotMyClass';

var_dump($a instanceof $b); // $b - объект класса MyClass
var_dump($a instanceof $c); // $c - строка 'MyClass'
var_dump($a instanceof $d); // $d - строка 'NotMyClass'
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
```

Оператор у станіне генерує жодних помилок, якщо перевірена змінна не є об'єктом. У цьому випадку він просто повертає **`false`**. Проте Константи не допускалися до PHP 7.3.0.

**Приклад #6 Приклад використання оператора `instanceof` для перевірки інших змінних**

```php
<?php
$a = 1;
$b = NULL;
$c = imagecreate(5, 5);
var_dump($a instanceof stdClass); // $a - целое типа integer
var_dump($b instanceof stdClass); // $b - NULL
var_dump($c instanceof stdClass); // $c - значение типа resource
var_dump(FALSE instanceof stdClass);
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(false)
bool(false)
PHP Fatal error:  instanceof expects an object instance, constant given
```

Починаючи з PHP 7.3.0, константи дозволені у лівій частині оператора `instanceof`

**Приклад #7 Використання `instanceof` для перевірки констант**

```php
<?php
var_dump(FALSE instanceof stdClass);
?>
```

Результат виконання цього прикладу в PHP 7.3:

```
bool(false)
```

Починаючи з PHP 8.0.0, `instanceof` тепер можна використовувати з довільними виразами. Вираз має бути поміщений у круглі дужки та являти собою рядок (string).

**Приклад #8 Приклад використання `instanceof` з довільним виразом**

```php
<?php

class ClassA extends \stdClass {}
class ClassB extends \stdClass {}
class ClassC extends ClassB {}
class ClassD extends ClassA {}

function getSomeClass(): string
{
    return ClassA::class;
}

var_dump(new ClassA instanceof ('std' . 'Class'));
var_dump(new ClassB instanceof ('Class' . 'B'));
var_dump(new ClassC instanceof ('Class' . 'A'));
var_dump(new ClassD instanceof (getSomeClass()));
?>
```

Результат виконання цього прикладу в PHP 8:

```
bool(true)
bool(true)
bool(false)
bool(true)
```

Оператор `instanceof` аналогічний функції [ісa()](function.is-a.md)

### Дивіться також

-   [getclass()](function.get-class.md)
-   [ісa()](function.is-a.md)
