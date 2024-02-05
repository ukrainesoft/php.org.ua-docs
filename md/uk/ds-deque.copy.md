---
navigation:
  - ds-deque.contains.md: '« Ds\\Deque::contains'
  - ds-deque.count.md: 'Ds\\Deque::count »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::copy

(PECL ds >= 1.0.0)

Ds\\Deque::copy — Повертає поверхневу копію колекції

### Опис

```methodsynopsis
public Ds\Deque::copy(): Ds\Deque
```

Повертає поверхневу копію двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія двосторонньої черги.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::copy()\*\*\*\*

```php
<?php
$a = new \Ds\Deque([1, 2, 3]);
$b = $a->copy();

$b->push(4);

print_r($a);
print_r($b);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```
