---
navigation:
  - ds-queue.push.md: '« Ds\\Queue::push'
  - class.ds-priorityqueue.md: Ds\\PriorityQueue »
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::toArray

(PECL ds >= 1.0.0)

Ds\\Queue::toArray — Перетворює колекцію на масив (array)

### Опис

```methodsynopsis
public Ds\Queue::toArray(): array
```

Перетворює колекцію на масив (array).

> **Зауваження** :
> 
> Приведення до типу array поки що не підтримується.

> **Зауваження** :
> 
> Цей метод не є руйнівним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить всі елементи колекції зі збереженням їхнього порядку.

### Приклади

**Пример #1 Пример использования метода**Ds\\Queue::toArray()\*\*\*\*

```php
<?php
$queue = new \Ds\Queue([1, 2, 3]);

var_dump($queue->toArray());
?>
```

Висновок наведеного прикладу буде схожим на:

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
