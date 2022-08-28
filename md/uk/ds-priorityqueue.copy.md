Повертає поверхневу копію черги

-   [« Ds\\PriorityQueue::\_\_construct](ds-priorityqueue.construct.html)
    
-   [Ds\\PriorityQueue::count »](ds-priorityqueue.count.html)
    
-   [PHP Manual](index.html)
    
-   [Очередь с приоритетом](class.ds-priorityqueue.html)
    
-   Повертає поверхневу копію черги
    

# ДсPriorityQueue::copy

(PECL ds >= 1.0.0)

ДсPriorityQueue::copy — Повертає поверхневу копію черги

### Опис

```methodsynopsis
public Ds\PriorityQueue::copy(): Ds\PriorityQueue
```

Повертає поверхневу копію черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія черги.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::copy()****

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->copy());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\PriorityQueue Object
(
    [0] => b
    [1] => c
    [2] => a
)
```