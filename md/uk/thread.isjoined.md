---
navigation:
  - thread.getthreadid.md: '« Thread::getThreadId'
  - thread.isstarted.md: 'Thread::isStarted »'
  - index.md: PHP Manual
  - class.thread.md: Thread
title: 'Thread::isJoined'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Повідомляє, чи приєднано вказаний потік**

```php
<?php
class My extends Thread {
    public function run() {
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
var_dump($my->isJoined());
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
```
