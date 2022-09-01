---
navigation:
  - ds-priorityqueue.allocate.html: '« DsPriorityQueue::allocate'
  - ds-priorityqueue.clear.html: 'ДсPriorityQueue::clear »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.html: Черга з пріоритетом
title: 'ДсPriorityQueue::capacity'
---
# ДсPriorityQueue::capacity

(PECL ds >= 1.0.0)

ДсPriorityQueue::capacity — Повертає поточну місткість

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

**Приклад #1 Приклад використання **ДсPriorityQueue::capacity()****

```php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(8)
```
