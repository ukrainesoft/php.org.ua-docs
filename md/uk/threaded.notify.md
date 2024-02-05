---
navigation:
  - threaded.merge.md: '« Threaded::merge'
  - threaded.notifyone.md: 'Threaded::notifyOne »'
  - index.md: PHP Manual
  - class.threaded.md: Threaded
title: 'Threaded::notify'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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
