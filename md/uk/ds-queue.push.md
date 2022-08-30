Додає значення в чергу

-   [« DsQueue::pop](ds-queue.pop.html)
    
-   [ДсQueue::toArray »](ds-queue.toarray.html)
    
-   [PHP Manual](index.md)
    
-   [Черга](class.ds-queue.html)
    
-   Додає значення в чергу
    

# ДсQueue::push

(PECL ds >= 1.0.0)

ДсQueue::push — Додає значення в чергу

### Опис

```methodsynopsis
public Ds\Queue::push(mixed ...$values): void
```

Додає значення `values` в чергу.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::push()****

```php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c", "d");
$queue->push(...["e", "f"]);

print_r($queue);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Queue Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```