---
navigation:
  - threaded.notify.md: '« Threaded::notify'
  - threaded.pop.md: 'Threaded::pop »'
  - index.md: PHP Manual
  - class.threaded.md: Threaded
title: 'Threaded::notifyOne'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

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

Результат виконання цього прикладу:

```
bool(true)
```
