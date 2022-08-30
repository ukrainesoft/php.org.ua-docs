Додає значення в чергу

-   [« DsPriorityQueue::pop](ds-priorityqueue.pop.html)
    
-   [ДсPriorityQueue::toArray »](ds-priorityqueue.toarray.html)
    
-   [PHP Manual](index.html)
    
-   [Черга з пріоритетом](class.ds-priorityqueue.html)
    
-   Додає значення в чергу
    

# ДсPriorityQueue::push

(PECL ds >= 1.0.0)

ДсPriorityQueue::push — Додає значення до черги

### Опис

```methodsynopsis
public Ds\PriorityQueue::push(mixed $value, int $priority): void
```

Додає `value` із заданим пріоритетом `priority` в чергу.

### Список параметрів

`value`

Значення, що додається.

`priority`

Пріоритет, з яким додається значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::push()****

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->pop());
print_r($queue->pop());
print_r($queue->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "b"
string(1) "c"
string(1) "a"
```