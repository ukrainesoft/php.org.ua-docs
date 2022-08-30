Повертає значення з початку черги

-   [« DsPriorityQueue::jsonSerialize](ds-priorityqueue.jsonserialize.html)
    
-   [ДсPriorityQueue::pop »](ds-priorityqueue.pop.html)
    
-   [PHP Manual](index.md)
    
-   [Черга з пріоритетом](class.ds-priorityqueue.html)
    
-   Повертає значення з початку черги
    

# ДсPriorityQueue::peek

(PECL ds >= 1.0.0)

ДсPriorityQueue::peek — Повертає значення з початку черги

### Опис

```methodsynopsis
public Ds\PriorityQueue::peek(): mixed
```

Повертає значення із початку черги, але не видаляє його.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення із початку черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо черга порожня.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::peek()****

```php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

var_dump($queue->peek());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "b"
```