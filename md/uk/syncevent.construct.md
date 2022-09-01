---
navigation:
  - class.syncevent.md: « SyncEvent
  - syncevent.fire.md: 'SyncEvent::fire »'
  - index.md: PHP Manual
  - class.syncevent.md: SyncEvent
title: 'SyncEvent::construct'
---
# SyncEvent::construct

(PECL sync >= 1.0.0)

SyncEvent::construct — Створення нового об'єкту SyncEvent

### Опис

```methodsynopsis
public SyncEvent::__construct(string $name = ?, bool $manual = false, bool $prefire = false)
```

Створює іменований чи безіменний об'єкт події.

### Список параметрів

`name`

Ім'я події, якщо це названий об'єкт події.

> **Зауваження**
> 
> Якщо ім'я вже існує, воно має бути доступним для відкриття поточним користувачем, від імені якого запущено процес, інакше буде викинуто виняток із безглуздим повідомленням про помилку.

`manual`

Визначає, чи потрібно скидати об'єкт події вручну.

> **Зауваження**
> 
> Об'єкти подій зі скиданням вручну дозволяють виконувати всі очікувані процеси, поки об'єкт не буде скинутий.

`prefire`

Визначає, чи потрібно заздалегідь активувати (сигналізувати) об'єкт події.

> **Зауваження**
> 
> Має значення тільки в тому випадку, якщо процес/потік, що викликає, першим створює об'єкт.

### Значення, що повертаються

Новий об'єкт [SyncEvent](class.syncevent.md)

### Помилки

Якщо об'єкт події не може бути створений або відкритий, викидається виняток.

### Приклади

**Приклад #1 Приклад використання **SyncEvent::construct()****

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

### список змін

| Версия | Описание |
| --- | --- |
| PECL sync 1.1.0 |  |
| Доданий параметр `prefire` |  |

### Дивіться також

-   [SyncEvent::fire()](syncevent.fire.md) - Запускає/встановлює подію
-   [SyncEvent::reset()](syncevent.reset.md) - скидає ручну подію
-   [SyncEvent::wait()](syncevent.wait.md) - Очікує запуску/установки події
