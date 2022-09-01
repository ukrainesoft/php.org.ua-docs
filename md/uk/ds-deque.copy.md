---
navigation:
  - ds-deque.contains.html: '« DsDeque::contains'
  - ds-deque.count.html: 'ДсDeque::count »'
  - index.md: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::copy'
---
# ДсDeque::copy

(PECL ds >= 1.0.0)

ДсDeque::copy — Повертає поверхневу копію колекції

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

**Приклад #1 Приклад використання **ДсDeque::copy()****

```php
<?php
$a = new \Ds\Deque([1, 2, 3]);
$b = $a->copy();

$b->push(4);

print_r($a);
print_r($b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
