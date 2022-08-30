Видаляє всі значення

-   [« DsPriorityQueue::capacity](ds-priorityqueue.capacity.html)
    
-   [ДсPriorityQueue::construct »](ds-priorityqueue.construct.html)
    
-   [PHP Manual](index.md)
    
-   [Черга з пріоритетом](class.ds-priorityqueue.html)
    
-   Видаляє всі значення
    

# ДсPriorityQueue::clear

(PECL ds >= 1.0.0)

ДсPriorityQueue::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\PriorityQueue::clear(): void
```

Видаляє всі значення з черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::clear()****

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

$queue->clear();
print_r($queue);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\PriorityQueue Object
(
)
```