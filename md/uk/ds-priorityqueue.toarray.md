Перетворює чергу на масив (array)

-   [« Ds\\PriorityQueue::push](ds-priorityqueue.push.html)
    
-   [var\_representation »](book.var_representation.html)
    
-   [PHP Manual](index.html)
    
-   [Очередь с приоритетом](class.ds-priorityqueue.html)
    
-   Перетворює чергу на масив (array)
    

# ДсPriorityQueue::toArray

(PECL ds >= 1.0.0)

ДсPriorityQueue::toArray — Перетворює чергу на масив (array)

### Опис

```methodsynopsis
public Ds\PriorityQueue::toArray(): array
```

Перетворює чергу на масив (array).

> **Зауваження**
> 
> Цей метод не є руйнівним.

> **Зауваження**
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить всі елементи черги із збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::toArray()****

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

var_dump($queue->toArray());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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