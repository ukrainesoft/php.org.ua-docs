---
navigation:
  - ds-priorityqueue.pop.md: '« Ds\\PriorityQueue::pop'
  - ds-priorityqueue.toarray.md: 'Ds\\PriorityQueue::toArray »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::push

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::push — Додає значення до черги

### Опис

```methodsynopsis
public Ds\PriorityQueue::push(mixed $value, int $priority): void
```

Добавляет`value` із заданим пріоритетом `priority` в чергу.

### Список параметрів

`value`

Значення, що додається.

`priority`

Пріоритет, з яким додається значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\PriorityQueue::push()\*\*\*\*

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
string(1) "b"
string(1) "c"
string(1) "a"
```
