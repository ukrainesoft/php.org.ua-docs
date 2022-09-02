---
navigation:
  - ds-set.reverse.md: '« DsSet::reverse'
  - ds-set.slice.md: 'ДсSet::slice »'
  - index.md: PHP Manual
  - class.ds-set.md: Набор
title: 'ДсSet::reversed'
---
# ДсSet::reversed

(PECL ds >= 1.0.0)

ДсSet::reversed — Повертає перегорнуту копію колекції

### Опис

```methodsynopsis
public Ds\Set::reversed(): Ds\Set
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Зауваження**
> 
> Поточна колекція не зміниться.

### Приклади

**Приклад #1 Приклад використання **ДсSet::reversed()****

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

print_r($set->reversed());
print_r($set);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
