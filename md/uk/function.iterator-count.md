---
navigation:
  - function.iterator-apply.html: « iteratorapply
  - function.iterator-to-array.html: iteratorтоarray »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: iteratorcount
---
# iteratorcount

(PHP 5> = 5.1.0, PHP 7, PHP 8)

iteratorcount — Підраховує кількість елементів в ітераторі

### Опис

```methodsynopsis
iterator_count(Traversable $iterator): int
```

Підраховує кількість елементів в ітераторі . **iteratorcount()** не гарантує збереження поточної позиції `iterator`

### Список параметрів

`iterator`

Ітератор, у якому провадиться підрахунок.

### Значення, що повертаються

Кількість елементів в ітераторі (`iterator`

### Приклади

**Приклад #1 Приклад використання **iteratorcount()****

```php
<?php
$iterator = new ArrayIterator(array('recipe'=>'pancakes', 'egg', 'milk', 'flour'));
var_dump(iterator_count($iterator));
?>
```

Результат виконання цього прикладу:

```
int(4)
```

**Приклад #2 **iteratorcount()** модифікує позицію**

```php
<?php
$iterator = new ArrayIterator(['one', 'two', 'three']);
var_dump($iterator->current());
var_dump(iterator_count($iterator));
var_dump($iterator->current());
?>
```

Результат виконання цього прикладу:

```
string(3) "one"
int(3)
NULL
```

**Приклад #3 **iteratorcount()** у циклі [foreach](control-structures.foreach.html)**

```php
<?php
$iterator = new ArrayIterator(['one', 'two', 'three']);
foreach ($iterator as $key => $value) {
    echo "$key: $value (", iterator_count($iterator), ")\n";
}?>
```

Результат виконання цього прикладу:

```
0: one (3)
```
