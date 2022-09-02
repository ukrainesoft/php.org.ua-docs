---
navigation:
  - ds-priorityqueue.pop.md: '« DsPriorityQueue::pop'
  - ds-priorityqueue.toarray.md: 'ДсPriorityQueue::toArray »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Черга з пріоритетом
title: 'ДсPriorityQueue::push'
---
# ДсPriorityQueue::push

(PECL ds >= 1.0.0)

ДсPriorityQueue::push — Додає значення до черги

### Опис

```methodsynopsis
public Ds\PriorityQueue::push(mixed $value, int $priority): void
```

Додає `value` із заданим пріоритетом `priority` в чергу.

### Список параметрів

`value`

Значення, що додається.

`priority`

Пріоритет, з яким додається значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::push()****

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->pop());
print_r($queue->pop());
print_r($queue->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "b"
string(1) "c"
string(1) "a"
```
