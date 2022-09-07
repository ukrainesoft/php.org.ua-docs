---
navigation:
  - ds-queue.capacity.md: '« DsQueue::capacity'
  - ds-queue.construct.md: 'ДсQueue::construct »'
  - index.md: PHP Manual
  - class.ds-queue.md: Черга
title: 'ДсQueue::clear'
---
# ДсQueue::clear

(PECL ds >= 1.0.0)

ДсQueue::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Queue::clear(): void
```

Видаляє всі значення з черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::clear()****

```php
<?php
$queue = new \Ds\Queue([1, 2, 3]);
print_r($queue);

$queue->clear();
print_r($queue);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Queue Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Queue Object
(
)
```
