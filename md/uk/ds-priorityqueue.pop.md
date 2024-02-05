---
navigation:
  - ds-priorityqueue.peek.md: '« Ds\\PriorityQueue::peek'
  - ds-priorityqueue.push.md: 'Ds\\PriorityQueue::push »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::pop

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::pop — Видаляє та повертає значення з найвищим пріоритетом

### Опис

```methodsynopsis
public Ds\PriorityQueue::pop(): mixed
```

Видаляє і повертає значення початку черги, тобто. значення із найвищим пріоритетом.

> **Зауваження** :
> 
> Значення з однаковим пріоритетом повертаються за принципом FIFO.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Видалене значення з початку черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо черга порожня.

### Приклади

**Пример #1 Пример использования**Ds\\PriorityQueue::pop()\*\*\*\*

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->pop());
print_r($queue->pop());
print_r($queue->pop());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
