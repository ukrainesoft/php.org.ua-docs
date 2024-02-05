---
navigation:
  - ds-stack.capacity.md: '« Ds\\Stack::capacity'
  - ds-stack.construct.md: 'Ds\\Stack::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::clear

(PECL ds >= 1.0.0)

Ds\\Stack::clear — Видаляє всі значення з колекції

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

**Приклад #1 Приклад використання** Ds\\Stack::clear()\*\*\*\*

```php
<?php
$stack = new \Ds\Stack([1, 2, 3]);
print_r($stack);

$stack->clear();
print_r($stack);
?>
```

Висновок наведеного прикладу буде схожим на:

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
