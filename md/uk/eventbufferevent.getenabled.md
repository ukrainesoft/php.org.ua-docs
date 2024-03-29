---
navigation:
  - eventbufferevent.getdnserrorstring.md: '« EventBufferEvent::getDnsErrorString'
  - eventbufferevent.getinput.md: 'EventBufferEvent::getInput »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::getEnabled'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::getEnabled

(PECL event >= 1.2.6-beta)

EventBufferEvent::getEnabled — Повертає бітову маску подій, які активовані для буферної події.

### Опис

```methodsynopsis
public
   EventBufferEvent::getEnabled(): int
```

Повертає бітову маску подій, які активовані для буферного події.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, що представляє бітову маску подій, які активовані для буферного події.

### Дивіться також

-   [EventBufferEvent::enable()](eventbufferevent.enable.md) \- Включає читання, запис або те й інше у події буфера
-   [EventBufferEvent::disable()](eventbufferevent.disable.md) \- Вимикає читання, запис або те й інше у події буфера
