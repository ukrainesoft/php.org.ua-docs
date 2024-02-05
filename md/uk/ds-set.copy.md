---
navigation:
  - ds-set.contains.md: '« Ds\\Set::contains'
  - ds-set.count.md: 'Ds\\Set::count »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::copy

(PECL ds >= 1.0.0)

Ds\\Set::copy — Повертає поверхневу копію колекції

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

**Приклад #1 Приклад використання** Ds\\Set::copy()\*\*\*\*

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->add(4);

print_r($a);
print_r($b);
?>
```

Висновок наведеного прикладу буде схожим на:

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
