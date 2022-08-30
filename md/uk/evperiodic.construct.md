Конструктор об'єкта спостерігача EvPeriodic

-   [« EvPeriodic::at](evperiodic.at.html)
    
-   [EvPeriodic::createStopped »](evperiodic.createstopped.html)
    
-   [PHP Manual](index.html)
    
-   [EvPeriodic](class.evperiodic.html)
    
-   Конструктор об'єкта спостерігача EvPeriodic
    

# EvPeriodic::construct

(PECL ev >= 0.2.0)

EvPeriodic::construct - Конструктор об'єкта спостерігача EvPeriodic

### Опис

public **EvPeriodic::construct**  
float `$offset`  
string `$interval`  
[callable](language.types.callable.html) `$reschedule_cb`  
[callable](language.types.callable.html) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` **`null`**  
int `$priority`

Створює об'єкт спостерігача EvPeriodic та запускає його автоматично. Метод [EvPeriodic::createStopped()](evperiodic.createstopped.html) створює зупинений періодичний спостерігач.

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
-   [EvTimer](class.evtimer.html)
-   [EvPeriodic::createStopped()](evperiodic.createstopped.html) - Створює зупинений спостерігач EvPeriodic