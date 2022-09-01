---
navigation:
  - eventbufferevent.setcallbacks.html: '« EventBufferEvent::setCallbacks'
  - eventbufferevent.settimeouts.html: 'EventBufferEvent::setTimeouts »'
  - index.html: PHP Manual
  - class.eventbufferevent.html: EventBufferEvent
title: 'EventBufferEvent::setPriority'
---
# EventBufferEvent::setPriority

(PECL event >= 1.2.6-beta)

EventBufferEvent::setPriority — Надає пріоритет bufferevent

### Опис

```methodsynopsis
public
   EventBufferEvent::setPriority(
    int
     $priority
   ): bool
```

Надає пріоритет bufferevent

**Увага**

Підтримується лише для подій буфера сокету

### Список параметрів

`priority`

Значення пріоритету.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
