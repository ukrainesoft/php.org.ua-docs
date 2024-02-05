---
navigation:
  - ds-set.get.md: '« Ds\\Set::get'
  - ds-set.isempty.md: 'Ds\\Set::isEmpty »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::intersect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::intersect

(PECL ds >= 1.0.0)

Ds\\Set::intersect — Створення нового набору, створеного перетином з іншим набором

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

### Дивіться також

-   [» Перетин](https://en.wikipedia.org/wiki/Intersection_(set_theory))на Вікіпедія

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::intersect()\*\*\*\*

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->intersect($b));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#3 (1) {
  [0]=>
  int(3)
}
```
