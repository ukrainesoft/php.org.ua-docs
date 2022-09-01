---
navigation:
  - class.event.md: « Event
  - event.addsignal.md: 'Event::addSignal »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::add'
---
# Event::add

(PECL event >= 1.2.6-beta)

Event::add — Перевести подію у стан очікування

### Опис

```methodsynopsis
public
   Event::add(
    float
     $timeout
    = ?): bool
```

Переводить подію у стан очікування. Події, що не очікують, ніколи не спрацюють і не викличуть callback-функцію. У поєднанні з [Event::del()](event.del.md), подія може бути перезаплановано користувачем у будь-який час.

Якщо метод **Event::add()** викликаний для вже очікуваної події, libevent залишить його в стані очікування і перезапланує його відповідно до заданого часу очікування (якщо воно задано). Якщо час очікування не заданий, то **Event::add()** не матиме будь-якого ефекту.

### Список параметрів

`timeout`

Час очікування за секунди.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додавання сигналу користувача**

```php
<?php
/*
Запустите в окне терминала:

$ php examples/signal.php

В другом окне терминала узнайте pid и отправьте SIGTERM, например:

$ ps aux | grep examp

ruslan    3976  0.2  0.0 139896 11256 pts/1    S+   10:25   0:00 php examples/signal.php
ruslan    3978  0.0  0.0   9572   864 pts/2    S+   10:26   0:00 grep --color=auto examp
$ kill -TERM 3976

В первом окне терминала вы должны увидеть следующее:
Пойманный сигнал 15
*/
class MyEventSignal {
    private $base, $ev;
    public function __construct($base) {
        $this->base = $base;
        $this->ev = Event::signal($base, SIGTERM, array($this, 'eventSighandler'));
        $this->ev->add();
    }
    public function eventSighandler($no, $c) {
        echo "Пойманный сигнал $no\n";
        $this->base->exit();
    }
}
$base = new EventBase();
$c    = new MyEventSignal($base);
$base->loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Пойманный сигнал 15
```

**Приклад #2 Додавання таймера**

```php
<?php
$base = new EventBase();
$n = 2;
$e = Event::timer($base, function($n) use (&$e) {
    echo "Прошло секунд: $n\n";
    $e->delTimer();
}, $n);
$e->add($n);
$base->loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Прошло секунд: 2
```

### Дивіться також

-   **Event::add()**
-   [Event::del()](event.del.md) - Перевести подію в пасивний стан
-   [Event::signal()](event.signal.md) - Створити об'єкт події сигналу
-   [Event::timer()](event.timer.md) - Створити об'єкт події таймера
