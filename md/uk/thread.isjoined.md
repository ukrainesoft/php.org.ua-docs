---
navigation:
  - thread.getthreadid.md: '« Thread::getThreadId'
  - thread.isstarted.md: 'Thread::isStarted »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::isJoined'
---
# Thread::isJoined

(PECL pthreads >= 2.0.0)

Thread::isJoined — Визначення стану

### Опис

```methodsynopsis
public Thread::isJoined(): bool
```

Повідомляє, чи було приєднано зазначений потік.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Повідомляє, чи приєднано вказаний потік**

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
var_dump($my->isJoined());
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
?>
```

Результат виконання цього прикладу:

```
bool(false)
```
