---
navigation:
  - threaded.synchronized.html: '« Threaded::synchronized'
  - class.thread.html: Thread »
  - index.html: PHP Manual
  - class.threaded.html: Threaded
title: 'Threaded::wait'
---
# Threaded::wait

(PECL pthreads >= 2.0.0)

Threaded::wait — Синхронізація

### Опис

```methodsynopsis
public Threaded::wait(int $timeout = ?): bool
```

Примушує викликаючий контекст чекати на повідомлення від зазначеного об'єкта.

### Список параметрів

`timeout`

Необов'язковий параметр часу очікування у мікросекундах.

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
