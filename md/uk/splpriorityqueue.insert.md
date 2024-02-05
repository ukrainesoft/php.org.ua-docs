---
navigation:
  - splpriorityqueue.getextractflags.md: '« SplPriorityQueue::getExtractFlags'
  - splpriorityqueue.iscorrupted.md: 'SplPriorityQueue::isCorrupted »'
  - index.md: PHP Manual
  - class.splpriorityqueue.md: SplPriorityQueue
title: 'SplPriorityQueue::insert'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplPriorityQueue::insert

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplPriorityQueue::insert — Додає елемент у чергу та пересортує її

### Опис

```methodsynopsis
public SplPriorityQueue::insert(mixed $value, mixed $priority): true
```

Добавляет значение`value`с приоритетом`priority` в чергу.

### Список параметрів

`value`

Значення, що додається.

`priority`

Пріоритет значення.

### Значення, що повертаються

Функція завжди повертає **`true`**
