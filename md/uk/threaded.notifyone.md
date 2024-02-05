---
navigation:
  - threaded.notify.md: '« Threaded::notify'
  - threaded.pop.md: 'Threaded::pop »'
  - index.md: PHP Manual
  - class.threaded.md: Threaded
title: 'Threaded::notifyOne'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Threaded::notifyOne

(PECL pthreads >= 3.0.0)

Threaded::notifyOne — Синхронізація

### Опис

```methodsynopsis
public Threaded::notifyOne(): bool
```

Надсилає повідомлення вказаному об'єкту. Це розблокує принаймні один із заблокованих потоків (на відміну від [Threaded::notify()](threaded.notify.md) з розблокуванням всіх потоків).

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
    $thread->notifyOne();
}, $my);
var_dump($my->join());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
