---
navigation:
  - eventbufferevent.setcallbacks.md: '« EventBufferEvent::setCallbacks'
  - eventbufferevent.settimeouts.md: 'EventBufferEvent::setTimeouts »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::setPriority'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
