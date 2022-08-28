Повертає поточну місткість

-   [« Ds\\PriorityQueue::allocate](ds-priorityqueue.allocate.html)
    
-   [Ds\\PriorityQueue::clear »](ds-priorityqueue.clear.html)
    
-   [PHP Manual](index.html)
    
-   [Очередь с приоритетом](class.ds-priorityqueue.html)
    
-   Повертає поточну місткість
    

# ДсPriorityQueue::capacity

(PECL ds >= 1.0.0)

ДсPriorityQueue::capacity — Повертає поточну місткість

### Опис

```methodsynopsis
public Ds\PriorityQueue::capacity(): int
```

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::capacity()****

```php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue->capacity());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(8)
```