---
navigation:
  - ds-pair.construct.md: '« Ds\\Pair::\_\_construct'
  - ds-pair.isempty.md: 'Ds\\Pair::isEmpty »'
  - index.md: PHP Manual
  - class.ds-pair.md: Ds\\Pair
title: 'Ds\\Pair::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Pair::copy

(No version information available, might only be in Git)

Ds\\Pair::copy — Повертає поверхневу копію пари

### Опис

```methodsynopsis
public Ds\Pair::copy(): Ds\Pair
```

Повертає поверхневу копію пари.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Ds\\Pair::copy()\*\*\*\*

```php
<?php
$a = new \Ds\Pair("a", 1);
$b = $a->copy();

$a->key = "x";

print_r($a);
print_r($b);
?>
```

Висновок наведеного прикладу буде схожим на:

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
