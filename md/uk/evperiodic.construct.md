---
navigation:
  - evperiodic.at.md: '« EvPeriodic::at'
  - evperiodic.createstopped.md: 'EvPeriodic::createStopped »'
  - index.md: PHP Manual
  - class.evperiodic.md: EvPeriodic
title: 'EvPeriodic::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvPeriodic::\_\_construct

(PECL ev >= 0.2.0)

EvPeriodic::\_\_construct - Конструктор об'єкта спостерігача EvPeriodic

### Опис

public**EvPeriodic::\_\_construct**  
float`$offset`  
string`$interval`  
[callable](language.types.callable.md) `$reschedule_cb`  
[callable](language.types.callable.md) `$callback`  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data` = **`null`**  
int`$priority` =  
) .

Створює об'єкт спостерігача EvPeriodic та запускає його автоматично. Метод [EvPeriodic::createStopped()](evperiodic.createstopped.md) створює зупинений періодичний спостерігач.

### Список параметрів

`offset`

Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`interval`

Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`reschedule_cb`

Перепризначити callback-функцію. Ви можете передати \*\*`null`\*\*Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`callback`

Смотрите[Спостерігачі callback-функції](ev.watcher-callbacks.md)

`data`

Ці дані, пов'язані зі спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Приклади

**Періодичний таймер. Використовуйте перепризначення callback-функції**

```php
<?php
// отмечает каждые 10.5 секунд

function reschedule_cb ($watcher, $now) {
 return $now + (10.5. - fmod($now, 10.5));
}

$w = new EvPeriodic(0., 0., "reschedule_cb", function ($w, $revents) {
 echo time(), PHP_EOL;
});
Ev::run();
?>
```

**Приклад #2 Періодичний таймер. Відзначає кожні 10,5 секунд, починаючи з поточного моменту**

```php
<?php
// Отмечает каждые 10.5 секунд, начиная с текущего момента
$w = new EvPeriodic(fmod(Ev::now(), 10.5), 10.5, NULL, function ($w, $revents) {
 echo time(), PHP_EOL;
});
Ev::run();
?>
```

**Приклад #3 Часовий спостерігач**

```php
<?php
$hourly = EvPeriodic(0, 3600, NULL, function () {
 echo "раз в час\n";
});
?>
```

### Дивіться також

-   [Періодичні режими роботи спостерігача](ev.periodic-modes.md)
-   [EvTimer](class.evtimer.md)
-   [EvPeriodic::createStopped()](evperiodic.createstopped.md) \- Створює зупинений спостерігач EvPeriodic
