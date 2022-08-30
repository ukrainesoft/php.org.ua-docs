Призначає callback-функції для читання, запису та події (стану)

-   [« EventBufferEvent::readBuffer](eventbufferevent.readbuffer.html)
    
-   [EventBufferEvent::setPriority »](eventbufferevent.setpriority.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Призначає callback-функції для читання, запису та події (стану)
    

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

Callback-функція читання. Дивіться докладніше [О callback-функциях буферов](eventbufferevent.about.callbacks.html)

`writecb`

Callback-функція запису. Дивіться докладніше [О callback-функциях буферов](eventbufferevent.about.callbacks.html)

`eventcb`

Callback – функція події зміни статусу. Дивіться докладніше [О callback-функциях буферов](eventbufferevent.about.callbacks.html)

`arg`

Змінна, яка буде передана всім callback-функціям.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventBufferEvent::construct()](eventbufferevent.construct.html) - Створює об'єкт EventBufferEvent