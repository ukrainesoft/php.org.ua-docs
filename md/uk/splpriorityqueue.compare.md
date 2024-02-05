---
navigation:
  - class.splpriorityqueue.md: « SplPriorityQueue
  - splpriorityqueue.count.md: 'SplPriorityQueue::count »'
  - index.md: PHP Manual
  - class.splpriorityqueue.md: SplPriorityQueue
title: 'SplPriorityQueue::compare'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplPriorityQueue::compare

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplPriorityQueue::compare — Порівнює пріоритети для коректного розміщення елементів у чергу

### Опис

```methodsynopsis
public SplPriorityQueue::compare(mixed $priority1, mixed $priority2): int
```

Сравнивает`priority1`с`priority2`

### Список параметрів

`priority1`

Пріоритет першого вузла.

`priority2`

Пріоритет другого вузла.

### Значення, що повертаються

Результат сравнения, положительное число, когда`priority1`больше`priority2`0 якщо вони рівні, і негативне число в інших випадках.

> **Зауваження** :
> 
> При додаванні кількох елементів з однаковим пріоритетом точний порядок прямування цих елементів у черзі не визначено.
