---
navigation:
  - function.get-declared-traits.html: « getdeclaredtraits
  - function.get-object-vars.html: getobjectvars »
  - index.html: PHP Manual
  - ref.classobj.html: Функції роботи з класами та об'єктами
title: getmangledobjectvars
---
# getmangledobjectvars

(PHP 7> = 7.4.0, PHP 8)

getmangledobjectvars — Повертає масив спотворених властивостей об'єкту

### Опис

```methodsynopsis
get_mangled_object_vars(object $object): array
```

Повертає масив (array), елементи якого властивості (змінні-члени) цього об'єкта. Ключами будуть імена змінних-членів з деякими примітними винятками: до закритих полів класу (private) попереду буде дописано ім'я класу; до захищених полів класу (protected) попереду буде додано символ `*`. Ці додані значення з обох сторін також мають `NUL` байти. Неініціалізовані [типізовані властивості](language.oop5.properties.html#language.oop5.properties.typed-properties) автоматично відкидаються.

### Список параметрів

`object`

Примірник об'єкта.

### Значення, що повертаються

Повертає масив (array), що містить усі властивості об'єкта `object`незалежно від області видимості.

### Приклади

**Приклад #1 Приклад використання **getmangledobjectvars()****

```php
<?php

class A
{
    public $public = 1;

    protected $protected = 2;

    private $private = 3;
}

class B extends A
{
    private $private = 4;
}

$object = new B;
$object->dynamic = 5;
$object->{'6'} = 6;

var_dump(get_mangled_object_vars($object));

class AO extends ArrayObject
{
    private $private = 1;
}

$arrayObject = new AO(['x' => 'y']);
$arrayObject->dynamic = 2;

var_dump(get_mangled_object_vars($arrayObject));
```

Результат виконання цього прикладу:

```
array(6) {
  ["Bprivate"]=>
  int(4)
  ["public"]=>
  int(1)
  ["*protected"]=>
  int(2)
  ["Aprivate"]=>
  int(3)
  ["dynamic"]=>
  int(5)
  [6]=>
  int(6)
}
array(2) {
  ["AOprivate"]=>
  int(1)
  ["dynamic"]=>
  int(2)
}
```

### Дивіться також

-   [getclassvars()](function.get-class-vars.html) - Повертає оголошені за умовчанням властивості класу
-   [getobjectvars()](function.get-object-vars.html) - Повертає властивості вказаного об'єкту
