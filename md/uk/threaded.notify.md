Синхронізація

-   [« Threaded::merge](threaded.merge.md)
    
-   [Threaded::notifyOne »](threaded.notifyone.md)
    
-   [PHP Manual](index.md)
    
-   [Threaded](class.threaded.md)
    
-   Синхронізація
    

# Threaded::notify

(PECL pthreads >= 2.0.0)

Threaded::notify — Синхронізація

### Опис

```methodsynopsis
public Threaded::notify(): bool
```

Надсилає повідомлення вказаному об'єкту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Сповіщення та очікування**

```php
<?php
class My extends Thread {
    public function run() {
        /** заставить этот поток ждать **/
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
/** отправить уведомление ожидающему потоку **/
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