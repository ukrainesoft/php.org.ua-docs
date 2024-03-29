---
navigation:
  - event.callbacks.md: « Callback-функції
  - class.event.md: Event »
  - index.md: PHP Manual
  - book.event.md: Event
title: Створення подій для сигналів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Створення подій для сигналів

Event може відстежувати сигнали у стилі POSIX. Для створення обробника сигналу використовуйте конструктор [Event::\_\_construct()](event.construct.md) з прапором **`Event::SIGNAL`** або фабричний метод [Event::signal()](event.signal.md)

**Приклад #1 Обработка сигнала`SIGTERM`**

```php
<?php
/*
Запускайте в окне терминала:

$ php examples/signal.php

В другом терминальном окне отыщите этот процесс и
пошлите ему сигнал SIGTERM:

$ ps aux | grep examp
ruslan    3976  0.2  0.0 139896 11256 pts/1    S+   10:25   0:00 php examples/signal.php
ruslan    3978  0.0  0.0   9572   864 pts/2    S+   10:26   0:00 grep --color=auto examp
$ kill -TERM 3976

В первом терминале вы увидите следующее:

Пойман сигнал 15
*/
class MyEventSignal {
    private $base, $ev;

    public function __construct($base) {
        $this->base = $base;
        $this->ev = Event::signal($base, SIGTERM, array($this, 'eventSighandler'));
        $this->ev->add();
    }

    public function eventSighandler($no, $c) {
        echo "Пойман сигнал $no\n";
        $this->base->exit();
    }
}

$base = new EventBase();
$c    = new MyEventSignal($base);

$base->loop();
?>
```

Зверніть увагу, що функції зворотного дзвінка запускаються всередині подієвого циклу після отримання сигналу, тому для них цілком безпечно викликати функції, які не слід запускати зі звичайних обробників сигналів POSIX.

Также почитайте[» Fast portable non-blocking network programming with Libevent, Constructing Signal Events](http://www.wangafu.net/~nickm/libevent-book/Ref4_event.md#_constructing_signal_events)
