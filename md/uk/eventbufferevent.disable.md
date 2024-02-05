---
navigation:
  - eventbufferevent.createpair.md: '« EventBufferEvent::createPair'
  - eventbufferevent.enable.md: 'EventBufferEvent::enable »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::disable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::disable

(PECL event >= 1.2.6-beta)

EventBufferEvent::disable — Вимикає читання, запис або те й інше в події буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::disable(
    int
     $events
   ): bool
```

Вимикає події **`Event::READ`** **`Event::WRITE`**, или\*\*`Event::READ`\*\* **`Event::WRITE`** у події буфера.

### Список параметрів

`events`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBufferEvent::enable()](eventbufferevent.enable.md) \- Включає читання, запис або те й інше у події буфера
