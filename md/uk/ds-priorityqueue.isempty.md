---
navigation:
  - ds-priorityqueue.count.md: '« DsPriorityQueue::count'
  - ds-priorityqueue.jsonserialize.md: 'ДсPriorityQueue::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Черга з пріоритетом
title: 'ДсPriorityQueue::isEmpty'
---
# ДсPriorityQueue::isEmpty

(PECL ds >= 1.0.0)

ДсPriorityQueue::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\PriorityQueue::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо черга порожня, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::isEmpty()****

```php
<?php
$a = new \Ds\PriorityQueue();
$b = new \Ds\PriorityQueue();

$a->push("a",  5);
$a->push("b", 15);
$a->push("c", 10);

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```
