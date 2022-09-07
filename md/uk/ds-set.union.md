---
navigation:
  - ds-set.toarray.md: '« DsSet::toArray'
  - ds-set.xor.md: 'ДсSet::xor »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::union'
---
# ДсSet::union

(PECL ds >= 1.0.0)

ДсSet::union — Створення нового набору з елементів поточного та переданого наборів

### Опис

```methodsynopsis
public Ds\Set::union(Ds\Set $set): Ds\Set
```

Створює новий набір з елементів поточного та переданого в `set` наборів.

`A ∪ B = {x: x ∈ A ∨ x ∈ B}`

### Список параметрів

`set`

Новий набір для об'єднання із поточним.

### Значення, що повертаються

Новий набір, що є об'єднанням поточного та переданого в `set`

### Також дивіться

-   [» Об'єднання](https://en.wikipedia.org/wiki/Union_(set_theory)) в Вікіпедія

### Приклади

**Приклад #1 Приклад використання **ДсSet::union()****

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->union($b));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#3 (5) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
}
```
