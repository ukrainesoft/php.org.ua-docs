---
navigation:
  - ds-priorityqueue.peek.md: '« DsPriorityQueue::peek'
  - ds-priorityqueue.push.md: 'ДсPriorityQueue::push »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Черга з пріоритетом
title: 'ДсPriorityQueue::pop'
---
# ДсPriorityQueue::pop

(PECL ds >= 1.0.0)

ДсPriorityQueue::pop — Видаляє та повертає значення з найвищим пріоритетом

### Опис

```methodsynopsis
public Ds\PriorityQueue::pop(): mixed
```

Видаляє і повертає значення початку черги, тобто. значення із найвищим пріоритетом.

> **Зауваження**
> 
> Значення з однаковим пріоритетом повертаються за принципом FIFO.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Видалене значення з початку черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо черга порожня.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::pop()****

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

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```
