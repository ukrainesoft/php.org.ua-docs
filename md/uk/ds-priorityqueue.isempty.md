---
navigation:
  - ds-priorityqueue.count.md: '« Ds\\PriorityQueue::count'
  - ds-priorityqueue.jsonserialize.md: 'Ds\\PriorityQueue::jsonSerialize »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::isEmpty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::isEmpty

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\PriorityQueue::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если очередь пуста,**`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Ds\\PriorityQueue::isEmpty()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```
