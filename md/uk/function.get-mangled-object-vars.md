---
navigation:
  - function.get-declared-traits.md: « get\_declared\_traits
  - function.get-object-vars.md: get\_object\_vars »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: get\_mangled\_object\_vars
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_mangled\_object\_vars

(PHP 7 >= 7.4.0, PHP 8)

get\_mangled\_object\_vars — Повертає масив спотворених властивостей об'єкту

### Опис

```methodsynopsis
get_mangled_object_vars(object $object): array
```

Повертає масив (array), елементи якого властивості (змінні-члени) цього об'єкта. Ключами будуть імена змінних-членів з деякими примітними винятками: до закритих полів класу (private) попереду буде дописано ім'я класу; до захищених полів класу (protected) попереду буде додано символ `*`. Ці додані значення з обох сторін також мають `NUL` байти. Неініціалізовані [типізовані властивості](language.oop5.properties.md#language.oop5.properties.typed-properties) автоматично відкидаються.

### Список параметрів

`object`

Примірник об'єкта.

### Значення, що повертаються

Повертає масив (array), що містить усі властивості об'єкта `object`незалежно від області видимості.

### Приклади

**Приклад #1 Приклад використання** get\_mangled\_object\_vars()\*\*\*\*

```php
<?php

class A
{
    public $public = 1;

    protected $protected = 2;

    private $private = 3;
}

class B extends A
{
    private $private = 4;
}

$object = new B;
$object->dynamic = 5;
$object->{'6'} = 6;

var_dump(get_mangled_object_vars($object));

class AO extends ArrayObject
{
    private $private = 1;
}

$arrayObject = new AO(['x' => 'y']);
$arrayObject->dynamic = 2;

var_dump(get_mangled_object_vars($arrayObject));
```

Результат виконання наведеного прикладу:

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

-   [get\_class\_vars()](function.get-class-vars.md) \- Повертає оголошені за умовчанням властивості класу
-   [get\_object\_vars()](function.get-object-vars.md) \- Повертає властивості вказаного об'єкту
