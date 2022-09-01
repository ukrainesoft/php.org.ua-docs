---
navigation:
  - ds-priorityqueue.capacity.html: '« DsPriorityQueue::capacity'
  - ds-priorityqueue.construct.html: 'ДсPriorityQueue::construct »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.html: Черга з пріоритетом
title: 'ДсPriorityQueue::clear'
---
# ДсPriorityQueue::clear

(PECL ds >= 1.0.0)

ДсPriorityQueue::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\PriorityQueue::clear(): void
```

Видаляє всі значення з черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::clear()****

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

$queue->clear();
print_r($queue);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\PriorityQueue Object
(
)
```
