---
navigation:
  - ds-priorityqueue.jsonserialize.md: '« Ds\\PriorityQueue::jsonSerialize'
  - ds-priorityqueue.pop.md: 'Ds\\PriorityQueue::pop »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::peek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::peek

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::peek — Повертає значення з початку черги

### Опис

```methodsynopsis
public Ds\PriorityQueue::peek(): mixed
```

Повертає значення із початку черги, але не видаляє його.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення із початку черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо черга порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\PriorityQueue::peek()\*\*\*\*

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

var_dump($queue->peek());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "b"
```
