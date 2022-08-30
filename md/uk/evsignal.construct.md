Конструктор об'єкта спостерігача EvSignal

-   [« EvSignal](class.evsignal.html)
    
-   [EvSignal::createStopped »](evsignal.createstopped.html)
    
-   [PHP Manual](index.html)
    
-   [EvSignal](class.evsignal.html)
    
-   Конструктор об'єкта спостерігача EvSignal
    

# EvSignal::construct

(PECL ev >= 0.2.0)

EvSignal::construct - Конструктор об'єкта спостерігача EvSignal

### Опис

public **EvSignal::construct**  
int `$signum`  
[callable](language.types.callable.html) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` **`null`**  
int `$priority`

Створює об'єкт спостерігач EvSignal та автоматично його запускає. Для створення зупиненого об'єкта спостерігача використовуйте метод [EvSignal::createStopped()](evsignal.createstopped.html)

### Список параметрів

`signum`

Номер сигналу. Дивіться константи модуля *pcntl* та документацію з `signal(7)`

`callback`

Дивіться [Функції зворотного виклику спостерігачів](ev.watcher-callbacks.html)

`data`

Дані користувача, асоційовані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Приклади

**Приклад #1 Обробка сигналу SIGTERM**

```php
<?php
$w = new EvSignal(SIGTERM, function ($watcher) {
    echo "SIGTERM received\n";
    $watcher->stop();
});

Ev::run();
?>
```

### Дивіться також

-   [EvSignal::createStopped()](evsignal.createstopped.html) - Create stopped EvSignal watcher object