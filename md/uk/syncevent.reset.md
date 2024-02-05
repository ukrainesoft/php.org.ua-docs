---
navigation:
  - syncevent.fire.md: '« SyncEvent::fire'
  - syncevent.wait.md: 'SyncEvent::wait »'
  - index.md: PHP Manual
  - class.syncevent.md: SyncEvent
title: 'SyncEvent::reset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncEvent::reset

(PECL sync >= 1.0.0)

SyncEvent::reset — Скидає ручну подію

### Опис

```methodsynopsis
public SyncEvent::reset(): bool
```

Скидає об'єкт [SyncEvent](class.syncevent.md), який було запущено/встановлено. Дійсно, тільки для об'єктів подій зі скиданням вручну.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1**SyncEvent::reset()**example**

```php
<?php
// В веб-приложении:
$event = new SyncEvent("DemoApplication", true);
$event->wait();

// В задании cron:
$event = new SyncEvent("DemoApplication", true);
$event->reset();
/* ... Выполнение некоторых задач по обслуживанию ... */
$event->fire();
?>
```

### Дивіться також

-   [SyncEvent::fire()](syncevent.fire.md) \- Запускає/встановлює подію
-   **SyncEvent::reset()**
-   [SyncEvent::wait()](syncevent.wait.md) \- Очікує запуску/установки події
