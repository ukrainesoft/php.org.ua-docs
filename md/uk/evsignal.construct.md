---
navigation:
  - class.evsignal.md: « EvSignal
  - evsignal.createstopped.md: 'EvSignal::createStopped »'
  - index.md: PHP Manual
  - class.evsignal.md: EvSignal
title: 'EvSignal::construct'
---
# EvSignal::construct

(PECL ev >= 0.2.0)

EvSignal::construct - Конструктор об'єкта спостерігача EvSignal

### Опис

public **EvSignal::construct**  
int `$signum`  
[callable](language.types.callable.md) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` **`null`**  
int `$priority`

Створює об'єкт спостерігач EvSignal та автоматично його запускає. Для створення зупиненого об'єкта спостерігача використовуйте метод [EvSignal::createStopped()](evsignal.createstopped.md)

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

-   [EvSignal::createStopped()](evsignal.createstopped.md) - Create stopped EvSignal watcher object
