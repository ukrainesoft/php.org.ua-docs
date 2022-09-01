---
navigation:
  - ds-priorityqueue.clear.html: '« DsPriorityQueue::clear'
  - ds-priorityqueue.copy.html: 'ДсPriorityQueue::copy »'
  - index.md: PHP Manual
  - class.ds-priorityqueue.html: Черга з пріоритетом
title: 'ДсPriorityQueue::construct'
---
# ДсPriorityQueue::construct

(PECL ds >= 1.0.0)

ДсPriorityQueue::construct — Створює новий екземпляр

### Опис

public **ДсPriorityQueue::construct**

Створює новий екземпляр.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::construct()****

```php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\PriorityQueue)#1 (0) {
}
```
