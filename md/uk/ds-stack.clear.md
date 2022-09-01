---
navigation:
  - ds-stack.capacity.html: '« DsStack::capacity'
  - ds-stack.construct.html: 'ДсStack::construct »'
  - index.md: PHP Manual
  - class.ds-stack.html: Стек
title: 'ДсStack::clear'
---
# ДсStack::clear

(PECL ds >= 1.0.0)

ДсStack::clear — Видаляє всі значення з колекції

### Опис

```methodsynopsis
public Ds\Stack::clear(): void
```

Видаляє всі значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсStack::clear()****

```php
<?php
$stack = new \Ds\Stack([1, 2, 3]);
print_r($stack);

$stack->clear();
print_r($stack);
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
)
```
