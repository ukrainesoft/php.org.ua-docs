---
navigation:
  - eventbufferevent.setpriority.html: '« EventBufferEvent::setPriority'
  - eventbufferevent.setwatermark.html: 'EventBufferEvent::setWatermark »'
  - index.html: PHP Manual
  - class.eventbufferevent.html: EventBufferEvent
title: 'EventBufferEvent::setTimeouts'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
