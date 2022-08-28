Повертає поточний розмір стека

-   [« Worker::collect](worker.collect.html)
    
-   [Worker::isShutdown »](worker.isshutdown.html)
    
-   [PHP Manual](index.html)
    
-   [Worker](class.worker.html)
    
-   Повертає поточний розмір стека
    

# Worker::getStacked

(PECL pthreads >= 2.0.0)

Worker::getStacked — Повертає поточний розмір стека

### Опис

```methodsynopsis
public Worker::getStacked(): int
```

Повертає кількість завдань, що залишилися у стеку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість завдань, що залишилися в стеку і чекають на запуск.

### Приклади

**Приклад #1 Приклад використання **Worker::getStacked****

```php
<?php
$worker = new Worker();

for ($i = 0; $i < 5; ++$i) {
    $worker->stack(new class extends Threaded {});
}

echo "There are {$worker->getStacked()} stacked tasks\n";
```

Результат виконання цього прикладу:

```
There are 5 stacked tasks
```