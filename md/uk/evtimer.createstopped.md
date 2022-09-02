---
navigation:
  - evtimer.construct.md: '« EvTimer::construct'
  - evtimer.set.md: 'EvTimer::set »'
  - index.md: PHP Manual
  - class.evtimer.md: EvTimer
title: 'EvTimer::createStopped'
---
# EvTimer::createStopped

(PECL ev >= 0.2.0)

EvTimer::createStopped — Створює зупинений спостерігач EvTimer

### Опис

```methodsynopsis
final
   public
   static
   EvTimer::createStopped(    
    float
     $after
   ,    
    float
     $repeat
   ,    
    callable
     $callback
   ,    
    mixed
     $data
     = null
   ,    
    int
     $priority
     = 0
   ): EvTimer
```

Створює зупинений спостерігач EvTimer. На відміну від [EvTimer::construct()](evtimer.construct.md), цей метод не запускає спостерігача автоматично.

### Список параметрів

`after`

Налаштовує таймер для запуску через `after` секунд.

`repeat`

Якщо час повтору дорівнює **`0.0`**, то він буде автоматично зупинено після закінчення часу очікування. Якщо позитивне, таймер буде автоматично налаштований на повторний запуск кожні повторювані секунди, доки не буде зупинено вручну.

`callback`

Дивіться [Спостерігачі callback-функцій](ev.watcher-callbacks.md)

`data`

Ці дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає об'єкт спостерігача EvTimer у разі успішного виконання.

### Приклади

**Приклад #1 Слідкуємо за змінами /var/log/messages. Уникаємо пропущені оновлення із затримкою в одну секунду**

```php
<?php
$timer = EvTimer::createStopped(0., 1.02, function ($w) {
    $w->stop();

    $stat = $w->data;

    // 1 секунда после последнего изменения файла
    printf("Текущий размер: %ld\n", $stat->attr()['size']);
});

$stat = new EvStat("/var/log/messages", 0., function () use ($timer) {
    // Сброс таймера наблюдателя
    $timer->again();
});

$timer->data = $stat;

Ev::run();
?>
```

### Дивіться також

-   [EvTimer::construct()](evtimer.construct.md) - Конструктор об'єкта спостерігача EvTimer
-   [EvPeriodic](class.evperiodic.md)
