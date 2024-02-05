---
navigation:
  - ds-collection.clear.md: '« Ds\\Collection::clear'
  - ds-collection.isempty.md: 'Ds\\Collection::isEmpty »'
  - index.md: PHP Manual
  - class.ds-collection.md: Ds\\Collection
title: 'Ds\\Collection::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Collection::copy

(PECL ds >= 1.0.0)

Ds\\Collection::copy — Повертає копію колекції

### Опис

```methodsynopsis
public Ds\Collection::copy(): Ds\Collection
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає копію колекції.

### Приклади

**Пример #1 Пример**Ds\\Collection::copy()\*\*\*\*

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = $a->copy();

$b->push(4);

print_r($a);
print_r($b);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```
