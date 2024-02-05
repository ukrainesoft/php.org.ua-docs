---
navigation:
  - ds-priorityqueue.capacity.md: '« Ds\\PriorityQueue::capacity'
  - ds-priorityqueue.construct.md: 'Ds\\PriorityQueue::\_\_construct »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::clear

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::clear — Видаляє всі значення

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

**Пример #1 Пример использования**Ds\\PriorityQueue::clear()\*\*\*\*

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

$queue->clear();
print_r($queue);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\PriorityQueue Object
(
)
```
