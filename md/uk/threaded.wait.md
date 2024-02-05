---
navigation:
  - threaded.synchronized.md: '« Threaded::synchronized'
  - class.thread.md: Thread »
  - index.md: PHP Manual
  - class.threaded.md: Threaded
title: 'Threaded::wait'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Сповіщення та очікування**

```php
<?php
class My extends Thread {
    public function run() {
        /** заставить этот поток ждать **/
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
/** отправить уведомление ожидающему потоку **/
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
var_dump($my->join());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
