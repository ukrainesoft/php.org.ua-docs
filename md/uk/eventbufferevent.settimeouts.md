---
navigation:
  - eventbufferevent.setpriority.md: '« EventBufferEvent::setPriority'
  - eventbufferevent.setwatermark.md: 'EventBufferEvent::setWatermark »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::setTimeouts'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::setTimeouts

(PECL event >= 1.2.6-beta)

EventBufferEvent::setTimeouts — Встановлює час очікування та запису для події буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::setTimeouts(
    float
     $timeout_read
   , 
    float
     $timeout_write
   ): bool
```

Встановлює час очікування читання та запису для події буфер

### Список параметрів

`timeout_read`

Час очікування читання

`timeout_write`

Час очікування запису

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
