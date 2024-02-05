---
navigation:
  - ds-priorityqueue.push.md: '« Ds\\PriorityQueue::push'
  - book.var_representation.md: var\_representation »
  - index.md: PHP Manual
  - class.ds-priorityqueue.md: Ds\\PriorityQueue
title: 'Ds\\PriorityQueue::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\PriorityQueue::toArray

(PECL ds >= 1.0.0)

Ds\\PriorityQueue::toArray — Перетворює чергу на масив (array)

### Опис

```methodsynopsis
public Ds\PriorityQueue::toArray(): array
```

Перетворює чергу на масив (array).

> **Зауваження** :
> 
> Цей метод не є руйнівним.

> **Зауваження** :
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить всі елементи черги, зберігаючи порядок, у якому вони зберігалися.

### Приклади

**Пример #1 Пример использования**Ds\\PriorityQueue::toArray()\*\*\*\*

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

var_dump($queue->toArray());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  string(1) "b"
  [1]=>
  string(1) "c"
  [2]=>
  string(1) "a"
}
```
