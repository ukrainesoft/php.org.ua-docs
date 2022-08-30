Створення подій для сигналів

-   [« Callback-функции](event.callbacks.html)
    
-   [Event »](class.event.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Створення подій для сигналів
    

# Створення подій для сигналів

Event може відстежувати сигнали у стилі POSIX. Для створення обробника сигналу використовуйте конструктор [Event::construct()](event.construct.html) з прапором **`Event::SIGNAL`** або фабричний метод [Event::signal()](event.signal.html)

**Приклад #1 Обробка сигналу `SIGTERM`**

```php
<?php
/*
Запускайте в окне терминала:

$ php examples/signal.php

В другом терминальном окне отыщите этот процесс и
пошлите ему сигнал SIGTERM:

$ ps aux | grep examp
ruslan    3976  0.2  0.0 139896 11256 pts/1    S+   10:25   0:00 php examples/signal.php
ruslan    3978  0.0  0.0   9572   864 pts/2    S+   10:26   0:00 grep --color=auto examp
$ kill -TERM 3976

В первом терминале вы увидите следующее:

Пойман сигнал 15
*/
class MyEventSignal {
    private $base, $ev;

    public function __construct($base) {
        $this->base = $base;
        $this->ev = Event::signal($base, SIGTERM, array($this, 'eventSighandler'));
        $this->ev->add();
    }

    public function eventSighandler($no, $c) {
        echo "Пойман сигнал $no\n";
        $this->base->exit();
    }
}

$base = new EventBase();
$c    = new MyEventSignal($base);

$base->loop();
?>
```

Зверніть увагу, що функції зворотного дзвінка запускаються всередині подієвого циклу після отримання сигналу, так що для них цілком безпечно викликати функції, які не слід запускати зі звичайних обробників сигналів POSIX.

Також почитайте [» Fast portable non-blocking network programming with Libevent, Constructing Signal Events](http://www.wangafu.net/~nickm/libevent-book/Ref4_event.html#_constructing_signal_events)