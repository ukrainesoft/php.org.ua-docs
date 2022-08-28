Видаляє всі значення

-   [« Ds\\Queue::capacity](ds-queue.capacity.html)
    
-   [Ds\\Queue::\_\_construct »](ds-queue.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Очередь](class.ds-queue.html)
    
-   Видаляє всі значення
    

# ДсQueue::clear

(PECL ds >= 1.0.0)

ДсQueue::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Queue::clear(): void
```

Видаляє всі значення з черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::clear()****

```php
<?php
$queue = new \Ds\Queue([1, 2, 3]);
print_r($queue);

$queue->clear();
print_r($queue);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Queue Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Queue Object
(
)
```