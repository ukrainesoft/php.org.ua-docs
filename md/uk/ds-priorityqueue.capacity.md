---
navigation:
  - ds-priorityqueue.allocate.md: '« Ds\\PriorityQueue::allocate'
  - ds-priorityqueue.clear.md: 'Ds\\PriorityQueue::clear »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::capacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::capacity

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\PriorityQueue::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання** Ds\\PriorityQueue::capacity()\*\*\*\*

```php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(8)
```
