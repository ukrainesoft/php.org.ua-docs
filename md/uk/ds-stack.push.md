---
navigation:
  - ds-stack.pop.md: '« Ds\\Stack::pop'
  - ds-stack.toarray.md: 'Ds\\Stack::toArray »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::push

(PECL ds >= 1.0.0)

Ds\\Stack::push — Додає значення до стек

### Опис

```methodsynopsis
public Ds\Stack::push(mixed ...$values): void
```

Добавляет значения`values` у стек

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Stack::push()\*\*\*\*

```php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c", "d");
$stack->push(...["e", "f"]);

print_r($stack);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Stack Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```
