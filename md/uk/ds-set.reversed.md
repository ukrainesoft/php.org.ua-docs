---
navigation:
  - ds-set.reverse.md: '« Ds\\Set::reverse'
  - ds-set.slice.md: 'Ds\\Set::slice »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::reversed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::reversed

(PECL ds >= 1.0.0)

Ds\\Set::reversed — Повертає перегорнуту копію колекції

### Опис

```methodsynopsis
public Ds\Set::reversed(): Ds\Set
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Зауваження** :
> 
> Поточна колекція не зміниться.

### Приклади

**Приклад #1 Приклад використання** Ds\\Set::reversed()\*\*\*\*

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

print_r($set->reversed());
print_r($set);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Set Object
(
    [0] => c
    [1] => b
    [2] => a
)
Ds\Set Object
(
    [0] => a
    [1] => b
    [2] => c
)
```
