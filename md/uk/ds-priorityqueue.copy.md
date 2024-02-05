---
navigation:
  - ds-priorityqueue.construct.md: '« Ds\\PriorityQueue::\_\_construct'
  - ds-priorityqueue.count.md: 'Ds\\PriorityQueue::count »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::copy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::copy

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::copy — Повертає поверхневу копію черги

### Опис

```methodsynopsis
public Ds\PriorityQueue::copy(): Ds\PriorityQueue
```

Повертає поверхневу копію черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія черги.

### Приклади

**Пример #1 Пример использования**Ds\\PriorityQueue::copy()\*\*\*\*

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->copy());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\PriorityQueue Object
(
    [0] => b
    [1] => c
    [2] => a
)
```
