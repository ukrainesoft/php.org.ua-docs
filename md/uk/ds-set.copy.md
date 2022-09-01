---
navigation:
  - ds-set.contains.html: '« DsSet::contains'
  - ds-set.count.html: 'ДсSet::count »'
  - index.md: PHP Manual
  - class.ds-set.html: Набор
title: 'ДсSet::copy'
---
# ДсSet::copy

(PECL ds >= 1.0.0)

ДсSet::copy — Повертає поверхневу копію колекції

### Опис

```methodsynopsis
public Ds\Set::copy(): Ds\Set
```

Повертає поверхневу копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція поверхнева копія.

### Приклади

**Приклад #1 Приклад використання **ДсSet::copy()****

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->add(4);

print_r($a);
print_r($b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Set Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Set Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```
