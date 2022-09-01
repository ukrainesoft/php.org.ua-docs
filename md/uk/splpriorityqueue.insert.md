---
navigation:
  - splpriorityqueue.getextractflags.html: '« SplPriorityQueue::getExtractFlags'
  - splpriorityqueue.iscorrupted.html: 'SplPriorityQueue::isCorrupted »'
  - index.html: PHP Manual
  - class.splpriorityqueue.html: SplPriorityQueue
title: 'SplPriorityQueue::insert'
---
# SplPriorityQueue::insert

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplPriorityQueue::insert — Додає елемент у чергу та пересортує її

### Опис

```methodsynopsis
public SplPriorityQueue::insert(mixed $value, mixed $priority): bool
```

Додає значення `value` з пріоритетом `priority` в чергу.

### Список параметрів

`value`

Значення, що додається.

`priority`

Пріоритет значення.

### Значення, що повертаються

Повертає **`true`**
