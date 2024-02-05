---
navigation:
  - ds-queue.allocate.md: '« Ds\\Queue::allocate'
  - ds-queue.clear.md: 'Ds\\Queue::clear »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::capacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::capacity

(PECL ds >= 1.0.0)

Ds\\Queue::capacity — Повертає поточну місткість

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

**Приклад #1 Приклад використання** Ds\\Queue::capacity()\*\*\*\*

```php
<?php
$queue = new \Ds\Queue();
var_dump($queue->capacity());

$queue->push(...range(1, 50));
var_dump($queue->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(8)
int(64)
```
