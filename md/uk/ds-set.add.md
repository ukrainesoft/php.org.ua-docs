---
navigation:
  - class.ds-set.html: « Набор
  - ds-set.allocate.html: 'ДсSet::allocate »'
  - index.md: PHP Manual
  - class.ds-set.html: Набор
title: 'ДсSet::add'
---
# ДсSet::add

(PECL ds >= 1.0.0)

ДсSet::add — Додає значення до набору

### Опис

```methodsynopsis
public Ds\Set::add(mixed ...$values): void
```

Додає всі задані значення набір, якщо вони раніше не були додані.

> **Зауваження**
> 
> Підтримуються значення типу об'єкта. Якщо об'єкт реалізує інтерфейс **ДсHashable**, перевірка здійснюється шляхом виклику методу об'єкта `equals`. Якщо об'єкт не реалізує інтерфейс **ДсHashable**, об'єкти повинні посилатися на той самий екземпляр класу.

**Застереження**

Усі порівняння суворі (за типом та значенням).

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSet::add()** зі скалярними значеннями**

```php
<?php
$set = new \Ds\Set();

$set->add(1);
$set->add(1);
$set->add(2);
$set->add(3);

// Производится строгое сравнение, поэтому "1" не приведётся к int(1)
$set->add("1");
$set->add(true);

var_dump($set);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#1 (5) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  string(1) "1"
  [4]=>
  bool(true)
}
```

**Приклад #2 Приклад використання **ДсSet::add()** з об'єктами**

```php
<?php
class HashableObject implements \Ds\Hashable
{
    /**
     * Произвольное значение для использования в качестве значения хеша.
     * Не определяет равенство.
     */
    private $value;

    public function __construct($value)
    {
        $this->value = $value;
    }

    public function hash()
    {
        return $this->value;
    }

    public function equals($obj): bool
    {
        return $this->value === $obj->value;
    }
}

$set = new \Ds\Set();

$obj = new \ArrayIterator([]);

// При добавлении одного и того же экземпляря несколько раз, добавится только первый.
$set->add($obj);
$set->add($obj);

// При добавлении нескольких экземпляров одного и того же объекта, они все добавятся.
$set->add(new \stdClass());
$set->add(new \stdClass());

// При добавлении объектов с одинаковым хешем несколько раз, добавится только первый.
$set->add(new \HashableObject(1));
$set->add(new \HashableObject(1));
$set->add(new \HashableObject(2));
$set->add(new \HashableObject(2));

var_dump($set);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#1 (5) {
  [0]=>
  object(ArrayIterator)#2 (1) {
    ["storage":"ArrayIterator":private]=>
    array(0) {
    }
  }
  [1]=>
  object(stdClass)#3 (0) {
  }
  [2]=>
  object(stdClass)#4 (0) {
  }
  [3]=>
  object(HashableObject)#5 (1) {
    ["value":"HashableObject":private]=>
    int(1)
  }
  [4]=>
  object(HashableObject)#6 (1) {
    ["value":"HashableObject":private]=>
    int(2)
  }
}
```
