Перевіряє, чи порожня колекція

-   [« DsPriorityQueue::count](ds-priorityqueue.count.html)
    
-   [ДсPriorityQueue::jsonSerialize »](ds-priorityqueue.jsonserialize.html)
    
-   [PHP Manual](index.md)
    
-   [Черга з пріоритетом](class.ds-priorityqueue.html)
    
-   Перевіряє, чи порожня колекція
    

# ДсPriorityQueue::isEmpty

(PECL ds >= 1.0.0)

ДсPriorityQueue::isEmpty — Перевіряє, чи порожня колекція

### Опис

```methodsynopsis
public Ds\PriorityQueue::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо черга порожня, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсPriorityQueue::isEmpty()****

```php
<?php
$a = new \Ds\PriorityQueue();
$b = new \Ds\PriorityQueue();

$a->push("a",  5);
$a->push("b", 15);
$a->push("c", 10);

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```