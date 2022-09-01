---
navigation:
  - ds-queue.push.html: '« DsQueue::push'
  - class.ds-priorityqueue.html: Черга з пріоритетом »
  - index.html: PHP Manual
  - class.ds-queue.html: Черга
title: 'ДсQueue::toArray'
---
# ДсQueue::toArray

(PECL ds >= 1.0.0)

ДсQueue::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Queue::toArray(): array
```

Перетворює колекцію на масив (array).

> **Зауваження**
> 
> Приведення до типу array поки що не підтримується.

> **Зауваження**
> 
> Цей метод не є руйнівним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить всі елементи колекції із збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::toArray()****

```php
<?php
$queue = new \Ds\Queue([1, 2, 3]);

var_dump($queue->toArray());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
