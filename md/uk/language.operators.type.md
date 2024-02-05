---
navigation:
  - language.operators.array.md: « Масиви
  - language.control-structures.md: Керуючі конструкції »
  - index.md: PHP Manual
  - language.operators.md: Оператори
title: Оператор перевірки типу
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Оператор перевірки типу

Оператор`instanceof` визначає, чи належить збережений в PHP-змінній об'єкт до конкретного [класу](language.oop5.basic.md#language.oop5.basic.class)

**Пример #1 Пример использования оператора`instanceof` з класами**

```php
<?php

class MyClass {}

class NotMyClass {}

$a = new MyClass();

var_dump($a instanceof MyClass);
var_dump($a instanceof NotMyClass);
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

Оператор`instanceof` також визначає, чи належить збережений у змінній об'єкт до класу-спадкоємця:

**Пример #2 Использование оператора`instanceof` з успадкованими класами**

```php
<?php

class ParentClass {}

class MyClass extends ParentClass {}

$a = new MyClass();

var_dump($a instanceof MyClass);
var_dump($a instanceof ParentClass);
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
```

Для перевірки *неприладдя* об'єкта класу, вказують [логічний оператор `not`](language.operators.logical.md)

**Пример #3 Использование оператора`instanceof` для перевірки того, що об'єкт - це *не* екземпляр класу**

```php
<?php

class MyClass {}

$a = new MyClass();
var_dump(!($a instanceof stdClass));
```

Результат виконання наведеного прикладу:

```
bool(true)
```

Наконец, оператор`instanceof` також перевіряє, чи реалізує об'єкт [інтерфейс](language.oop5.interfaces.md) :

**Пример #4 Использование оператора`instanceof` з інтерфейсами**

```php
<?php

interface MyInterface {}

class MyClass implements MyInterface {}

$a = new MyClass();

var_dump($a instanceof MyClass);
var_dump($a instanceof MyInterface);
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
```

Хотя оператор`instanceof` зазвичай вказують з буквальним ім'ям класу, його можна також вказувати зі змінною об'єкта або рядковою змінною:

**Пример #5 Использование оператора`instanceof` з іншими змінними**

```php
<?php

interface MyInterface {}

class MyClass implements MyInterface {}

$a = new MyClass();
$b = new MyClass();
$c = 'MyClass';
$d = 'NotMyClass';
var_dump($a instanceof $b); // $b — объект класса MyClass
var_dump($a instanceof $c); // $c — строка 'MyClass'
var_dump($a instanceof $d); // $d — строка 'NotMyClass'
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
```

Оператор instanceof не викидає жодних помилок, якщо змінна, що перевіряється - не об'єкт, він просто повертає **`false`**. Константи, однак, не було дозволено до PHP 7.3.0.

**Пример #6 Пример использования оператора`instanceof` для перевірки інших змінних**

```php
<?php

$a = 1;
$b = NULL;
$c = imagecreate(5, 5);
var_dump($a instanceof stdClass); // $a — целое типа integer
var_dump($b instanceof stdClass); // $b — NULL
var_dump($c instanceof stdClass); // $c — значение типа resource
var_dump(FALSE instanceof stdClass);
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(false)
bool(false)
PHP Fatal error:  instanceof expects an object instance, constant given
```

Починаючи з PHP 7.3.0, константи дозволені в лівій частині оператора `instanceof`

**Пример #7 Использование`instanceof` для перевірки констант**

```php
<?php

var_dump(FALSE instanceof stdClass);
```

Результат виконання наведеного прикладу в PHP 7.3:

```
bool(false)
```

Починаючи з PHP 8.0.0 `instanceof` можна використовувати з довільними виразами. Вираз має бути поміщений у круглі дужки та бути рядком (string).

**Пример #8 Пример использования`instanceof` з довільним виразом**

```php
<?php

class ClassA extends \stdClass {}
class ClassB extends \stdClass {}
class ClassC extends ClassB {}
class ClassD extends ClassA {}

function getSomeClass(): string
{
    return ClassA::class;
}

var_dump(new ClassA instanceof ('std' . 'Class'));
var_dump(new ClassB instanceof ('Class' . 'B'));
var_dump(new ClassC instanceof ('Class' . 'A'));
var_dump(new ClassD instanceof (getSomeClass()));
```

Результат виконання наведеного прикладу в PHP 8:

```
bool(true)
bool(true)
bool(false)
bool(true)
```

Оператор`instanceof` аналогічний функції [is\_a()](function.is-a.md)

### Дивіться також

-   [get\_class()](function.get-class.md)
-   [is\_a()](function.is-a.md)
