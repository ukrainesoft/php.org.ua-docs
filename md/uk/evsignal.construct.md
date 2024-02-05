---
navigation:
  - class.evsignal.md: « EvSignal
  - evsignal.createstopped.md: 'EvSignal::createStopped »'
  - index.md: PHP Manual
  - class.evsignal.md: EvSignal
title: 'EvSignal::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvSignal::\_\_construct

(PECL ev >= 0.2.0)

EvSignal::\_\_construct - Конструктор об'єкта спостерігача EvSignal

### Опис

public **EvSignal::\_\_construct**  
int`$signum`  
[callable](language.types.callable.md) `$callback`  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data` = **`null`**  
int`$priority` =  
) .

Створює об'єкт спостерігач EvSignal та автоматично його запускає. Для створення зупиненого об'єкта спостерігача використовуйте метод [EvSignal::createStopped()](evsignal.createstopped.md)

### Список параметрів

`signum`

Номер сигналу. Дивіться константи модуля *pcntl*и документацию по`signal(7)`

`callback`

Смотрите[Функції зворотного виклику спостерігачів](ev.watcher-callbacks.md)

`data`

Дані користувача, асоційовані з спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Приклади

**Приклад #1 Обробка сигналу SIGTERM**

```php
<?php
$w = new EvSignal(SIGTERM, function ($watcher) {
    echo "SIGTERM received\n";
    $watcher->stop();
});

Ev::run();
?>
```

### Дивіться також

-   [EvSignal::createStopped()](evsignal.createstopped.md) \- Create stopped EvSignal watcher object
