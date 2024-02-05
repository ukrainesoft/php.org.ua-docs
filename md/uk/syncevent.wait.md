---
navigation:
  - syncevent.reset.md: '« SyncEvent::reset'
  - class.syncreaderwriter.md: SyncReaderWriter »
  - index.md: PHP Manual
  - class.syncevent.md: SyncEvent
title: 'SyncEvent::wait'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncEvent::wait

(PECL sync >= 1.0.0)

SyncEvent::wait — Очікує запуску/установки події

### Опис

```methodsynopsis
public SyncEvent::wait(int $wait = -1): bool
```

Чекає на запуск об'єкта [SyncEvent](class.syncevent.md)

### Список параметрів

`wait`

Кількість мілісекунд очікування запуску події. Значення -1 нескінченне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SyncEvent::wait()\*\*\*\*

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

-   [SyncEvent::fire()](syncevent.fire.md) \- Запускає/встановлює подію
