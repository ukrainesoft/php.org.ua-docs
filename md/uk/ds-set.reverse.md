---
navigation:
  - ds-set.remove.html: '« DsSet::remove'
  - ds-set.reversed.html: 'ДсSet::reversed »'
  - index.html: PHP Manual
  - class.ds-set.html: Набор
title: 'ДсSet::reverse'
---
# ДсSet::reverse

(PECL ds >= 1.0.0)

ДсSet::reverse — Перевертає поточну колекцію

### Опис

```methodsynopsis
public Ds\Set::reverse(): void
```

Перевертає поточну колекцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSet::reverse()****

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);
$set->reverse();

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
```
