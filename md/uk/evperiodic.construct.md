---
navigation:
  - evperiodic.at.md: '« EvPeriodic::at'
  - evperiodic.createstopped.md: 'EvPeriodic::createStopped »'
  - index.md: PHP Manual
  - class.evperiodic.md: EvPeriodic
title: 'EvPeriodic::construct'
---
# EvPeriodic::construct

(PECL ev >= 0.2.0)

EvPeriodic::construct - Конструктор об'єкта спостерігача EvPeriodic

### Опис

public **EvPeriodic::construct**  
float `$offset`  
string `$interval`  
[callable](language.types.callable.md) `$reschedule_cb`  
[callable](language.types.callable.md) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` **`null`**  
int `$priority`

Створює об'єкт спостерігача EvPeriodic та запускає його автоматично. Метод [EvPeriodic::createStopped()](evperiodic.createstopped.md) створює зупинений періодичний спостерігач.

### Список параметрів

`offset`

Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.html)

`interval`

Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.html)

`reschedule_cb`

Перепризначити callback-функцію. Ви можете передати **`null`**. Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.html)

`callback`

Дивіться [Спостерігачі callback-функції](ev.watcher-callbacks.html)

`data`

Дані користувача, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Приклади

**Періодичний таймер. Використовуйте перепризначення callback-функції**

```php
<?php
// отмечает каждые 10.5 секунд

function reschedule_cb ($watcher, $now) {
 return $now + (10.5. - fmod($now, 10.5));
}

$w = new EvPeriodic(0., 0., "reschedule_cb", function ($w, $revents) {
 echo time(), PHP_EOL;
});
Ev::run();
?>
```

**Приклад #2 Періодичний таймер. Відзначає кожні 10,5 секунд, починаючи з поточного моменту**

```php
<?php
// Отмечает каждые 10.5 секунд, начиная с текущего момента
$w = new EvPeriodic(fmod(Ev::now(), 10.5), 10.5, NULL, function ($w, $revents) {
 echo time(), PHP_EOL;
});
Ev::run();
?>
```

**Приклад #3 Часовий спостерігач**

```php
<?php
$hourly = EvPeriodic(0, 3600, NULL, function () {
 echo "раз в час\n";
});
?>
```

### Дивіться також

-   [Періодичні режими роботи спостерігача](ev.periodic-modes.html)
-   [EvTimer](class.evtimer.md)
-   [EvPeriodic::createStopped()](evperiodic.createstopped.md) - Створює зупинений спостерігач EvPeriodic
