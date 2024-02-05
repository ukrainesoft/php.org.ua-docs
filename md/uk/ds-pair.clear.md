---
navigation:
  - class.ds-pair.md: « Ds\\Pair
  - ds-pair.construct.md: 'Ds\\Pair::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-pair.md: Ds\\Pair
title: 'Ds\\Pair::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Pair::clear

(No version information available, might only be in Git)

Ds\\Pair::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Pair::clear(): void
```

Видаляє всі значення з пари.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Pair::clear()\*\*\*\*

```php
<?php
$pair = new \Ds\Pair("a", 1);
print_r($pair);

$pair->clear();
print_r($pair);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Pair Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Pair Object
(
)
```
