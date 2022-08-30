Вимикає читання, запис або те й інше в події буфера

-   [« EventBufferEvent::createPair](eventbufferevent.createpair.md)
    
-   [EventBufferEvent::enable »](eventbufferevent.enable.md)
    
-   [PHP Manual](index.md)
    
-   [EventBufferEvent](class.eventbufferevent.md)
    
-   Вимикає читання, запис або те й інше в події буфера
    

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

Вимикає події **`Event::READ`** **`Event::WRITE`**, або **`Event::READ`** `|` **`Event::WRITE`** у події буфера.

### Список параметрів

`events`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBufferEvent::enable()](eventbufferevent.enable.md) - Включає читання, запис або те й інше у події буфера