Визначення стану

-   [« Threaded::extend](threaded.extend.html)
    
-   [Threaded::isTerminated »](threaded.isterminated.html)
    
-   [PHP Manual](index.html)
    
-   [Threaded](class.threaded.html)
    
-   Визначення стану
    

# Threaded::isRunning

(PECL pthreads >= 2.0.0)

Threaded::isRunning — Визначення стану

### Опис

```methodsynopsis
public Threaded::isRunning(): bool
```

Повідомляє, чи вказаний об'єкт виконується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Логічне значення стану об'єкта.

> **Зауваження**
> 
> Об'єкт вважається запущеним під час виконання методу run.

### Приклади

**Приклад #1 Визначення стану вказаного об'єкта**

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
var_dump($my->isRunning());
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
?>
```

Результат виконання цього прикладу:

```
bool(true)
```