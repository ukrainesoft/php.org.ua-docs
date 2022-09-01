---
navigation:
  - syncevent.construct.html: '« SyncEvent::construct'
  - syncevent.reset.html: 'SyncEvent::reset »'
  - index.html: PHP Manual
  - class.syncevent.html: SyncEvent
title: 'SyncEvent::fire'
---
# SyncEvent::fire

(PECL sync >= 1.0.0)

SyncEvent::fire — Запускає/встановлює подію

### Опис

```methodsynopsis
public SyncEvent::fire(): bool
```

Запускає/встановлює об'єкт [SyncEvent](class.syncevent.html). Дозволяє проходити кільком потокам, які очікують, якщо об'єкт події був створений з параметром manual рівним **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncEvent::fire()****

```php
<?php
// В веб-приложении:
$event = new SyncEvent("GetAppReport");
$event->fire();

// В задании cron:
$event = new SyncEvent("GetAppReport");
$event->wait();
?>
```

### Дивіться також

-   [SyncEvent::reset()](syncevent.reset.html) - скидає ручну подію
-   [SyncEvent::wait()](syncevent.wait.html) - Очікує запуску/установки події
