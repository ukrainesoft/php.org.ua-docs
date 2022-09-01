---
navigation:
  - ds-pair.construct.html: '« DsPair::construct'
  - ds-pair.isempty.html: 'ДсPair::isEmpty »'
  - index.md: PHP Manual
  - class.ds-pair.html: Пара
title: 'ДсPair::copy'
---
# ДсPair::copy

(No version information available, might only be in Git)

ДсPair::copy — Повертає поверхневу копію пари

### Опис

```methodsynopsis
public Ds\Pair::copy(): Ds\Pair
```

Повертає поверхневу копію пари.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **ДсPair::copy()****

```php
<?php
$a = new \Ds\Pair("a", 1);
$b = $a->copy();

$a->key = "x";

print_r($a);
print_r($b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Pair Object
(
    [key] => x
    [value] => 1
)
Ds\Pair Object
(
    [key] => a
    [value] => 1
)
```
