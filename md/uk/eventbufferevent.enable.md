---
navigation:
  - eventbufferevent.disable.md: '« EventBufferEvent::disable'
  - eventbufferevent.free.md: 'EventBufferEvent::free »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::enable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::enable

(PECL event >= 1.2.6-beta)

EventBufferEvent::enable — Включає читання, запис або те й інше в події буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::enable(
    int
     $events
   ): bool
```

Включає події **`Event::READ`** **`Event::WRITE`**, или\*\*`Event::READ`\*\* **`Event::WRITE`** у події буфера.

### Список параметрів

`events`

**`Event::READ`** **`Event::WRITE`**, или\*\*`Event::READ`\*\* **`Event::WRITE`** у події буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBufferEvent::disable()](eventbufferevent.disable.md) \- Вимикає читання, запис або те й інше у події буфера
