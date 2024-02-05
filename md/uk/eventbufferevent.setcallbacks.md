---
navigation:
  - eventbufferevent.readbuffer.md: '« EventBufferEvent::readBuffer'
  - eventbufferevent.setpriority.md: 'EventBufferEvent::setPriority »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::setCallbacks'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::setCallbacks

(PECL event >= 1.2.6-beta)

EventBufferEvent::setCallbacks — Призначає callback-функції для читання, запису та події (стану)

### Опис

```methodsynopsis
public
   EventBufferEvent::setCallbacks(    
    callable
     $readcb
   ,    
    callable
     $writecb
   ,    
    callable
     $eventcb
   ,    
    mixed
     $arg
    = ?): void
```

Призначає callback-функції для читання, запису та події (стану).

### Список параметрів

`readcb`

Callback-функция чтения. Смотрите подробнее[Про callback-функції буферів](eventbufferevent.about.callbacks.md)

`writecb`

Callback-функция записи. Смотрите подробнее[Про callback-функції буферів](eventbufferevent.about.callbacks.md)

`eventcb`

Callback – функція події зміни статусу. Дивіться докладніше [Про callback-функції буферів](eventbufferevent.about.callbacks.md)

`arg`

Змінна, яка буде передана всім callback-функціям.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventBufferEvent::\_\_construct()](eventbufferevent.construct.md) \- Створює об'єкт EventBufferEvent
