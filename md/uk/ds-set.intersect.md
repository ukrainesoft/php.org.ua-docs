---
navigation:
  - ds-set.get.md: '« DsSet::get'
  - ds-set.isempty.md: 'ДсSet::isEmpty »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::intersect'
---
# ДсSet::intersect

(PECL ds >= 1.0.0)

ДсSet::intersect — Створення нового набору, створеного перетином з іншим набором

### Опис

```methodsynopsis
public Ds\Set::intersect(Ds\Set $set): Ds\Set
```

Створює новий набір, що містить значення, які присутні у поточному наборі та наборі, переданому параметром `set`

`A ∩ B = {x : x ∈ A ∧ x ∈ B}`

### Список параметрів

`set`

Новий набір типу Set.

### Значення, що повертаються

Перетин поточного набору та переданого в `set`

### Також дивіться

-   [» Перетин](https://en.wikipedia.org/wiki/Intersection_(set_theory)) на Вікіпедія

### Приклади

**Приклад #1 Приклад використання **ДсSet::intersect()****

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->intersect($b));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#3 (1) {
  [0]=>
  int(3)
}
```
