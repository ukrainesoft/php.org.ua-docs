---
navigation:
  - ds-queue.construct.md: '« DsQueue::construct'
  - ds-queue.count.md: 'ДсQueue::count »'
  - index.md: PHP Manual
  - class.ds-queue.md: Черга
title: 'ДсQueue::copy'
---
# ДсQueue::copy

(PECL ds >= 1.0.0)

ДсQueue::copy — Повертає поверхневу копію черги

### Опис

```methodsynopsis
public Ds\Queue::copy(): Ds\Queue
```

Повертає поверхневу копію черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія черги.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::copy()****

```php
<?php
$a = new \Ds\Queue([1, 2, 3]);
$b = $a->copy();

// Изменение копии не отражается на оригинале
$b->push(4);

print_r($a);
print_r($b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Queue Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Queue Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```
