---
navigation:
  - syncevent.construct.md: '« SyncEvent::construct'
  - syncevent.reset.md: 'SyncEvent::reset »'
  - index.md: PHP Manual
  - class.syncevent.md: SyncEvent
title: 'SyncEvent::fire'
---
# SyncEvent::fire

(PECL sync >= 1.0.0)

SyncEvent::fire — Запускає/встановлює подію

### Опис

```methodsynopsis
public SyncEvent::fire(): bool
```

Запускає/встановлює об'єкт [SyncEvent](class.syncevent.md). Дозволяє проходити кільком потокам, які очікують, якщо об'єкт події був створений з параметром manual рівним **`true`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncEvent::fire()****

```php
<?php
// В веб-приложении:
$event = new SyncEvent("GetAppReport");
$event->fire();

// В задании cron:
$event = new SyncEvent("GetAppReport");
$event->wait();
?>
```

### Дивіться також

-   [SyncEvent::reset()](syncevent.reset.md) - скидає ручну подію
-   [SyncEvent::wait()](syncevent.wait.md) - Очікує запуску/установки події
