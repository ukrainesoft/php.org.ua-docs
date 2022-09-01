---
navigation:
  - ds-stack.construct.html: '« DsStack::construct'
  - ds-stack.count.html: 'ДсStack::count »'
  - index.md: PHP Manual
  - class.ds-stack.html: Стек
title: 'ДсStack::copy'
---
# ДсStack::copy

(PECL ds >= 1.0.0)

ДсStack::copy — Повертає поверхневу копію колекції

### Опис

```methodsynopsis
public Ds\Stack::copy(): Ds\Stack
```

Повертає поверхневу копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція поверхнева копія.

### Приклади

**Приклад #1 Приклад використання **ДсStack::copy()****

```php
<?php
$a = new \Ds\Stack([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->push(4);

print_r($a);
print_r($b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Stack Object
(
    [0] => 3
    [1] => 2
    [2] => 1
)
Ds\Stack Object
(
    [0] => 4
    [1] => 3
    [2] => 2
    [3] => 1
)
```
