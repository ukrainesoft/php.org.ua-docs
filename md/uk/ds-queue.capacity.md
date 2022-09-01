---
navigation:
  - ds-queue.allocate.html: '« DsQueue::allocate'
  - ds-queue.clear.html: 'ДсQueue::clear »'
  - index.html: PHP Manual
  - class.ds-queue.html: Черга
title: 'ДсQueue::capacity'
---
# ДсQueue::capacity

(PECL ds >= 1.0.0)

ДсQueue::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\Queue::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::capacity()****

```php
<?php
$queue = new \Ds\Queue();
var_dump($queue->capacity());

$queue->push(...range(1, 50));
var_dump($queue->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(8)
int(64)
```
