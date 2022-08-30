Синхронізація

-   [« Threaded::shift](threaded.shift.md)
    
-   [Threaded::wait »](threaded.wait.md)
    
-   [PHP Manual](index.md)
    
-   [Threaded](class.threaded.md)
    
-   Синхронізація
    

# Threaded::synchronized

(PECL pthreads >= 2.0.0)

Threaded::synchronized — Синхронізація

### Опис

```methodsynopsis
public Threaded::synchronized(Closure $block, mixed ...$args): mixed
```

Виконує блок, зберігаючи блокування синхронізації посилальних об'єктів для контексту, що викликає.

### Список параметрів

`block`

Блок коду для виконання.

`args`

Список аргументів змінної довжини для використання як аргументи функції блоку.

### Значення, що повертаються

Значення блоку, що повертається.

### Приклади

**Приклад #1 Синхронізація**

```php
<?php
class My extends Thread {
    public function run() {
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
var_dump($my->join());
?>
```

Результат виконання цього прикладу:

```
bool(true)
```