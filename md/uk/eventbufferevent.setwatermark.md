Регулює водяні знаки читання та/або запису

-   [« EventBufferEvent::setTimeouts](eventbufferevent.settimeouts.md)
    
-   [EventBufferEvent::sslError »](eventbufferevent.sslerror.md)
    
-   [PHP Manual](index.md)
    
-   [EventBufferEvent](class.eventbufferevent.md)
    
-   Регулює водяні знаки читання та/або запису
    

# EventBufferEvent::setWatermark

(PECL event >= 1.2.6-beta)

EventBufferEvent::setWatermark — Регулює водяні знаки читання та/або запису

### Опис

```methodsynopsis
public
   EventBufferEvent::setWatermark(
    int
     $events
   , 
    int
     $lowmark
   , 
    int
     $highmark
   ): void
```

Регулює водяні знаки читання, *водяні знаки* записи або й те, й інше для однієї події буфера.

Водяний знак події буфера – це значення, що визначає кількість байтів, які мають бути прочитані чи записані перед викликом callback-функції. За замовчуванням, кожна подія читання/запису запускає виклик callback-функції. Зверніться до [» Fast portable non-blocking network programming with Libevent: Callbacks and watermarks](http://www.wangafu.net/~nickm/libevent-book/Ref6_bufferevent.html#_callbacks_and_watermarks)

### Список параметрів

`events`

Бітова маска **`Event::READ`** **`Event::WRITE`** або обох.

`lowmark`

Мінімальне значення водяний знак.

`highmark`

Максимальне значення водяного знаку . **`0`** означає "без обмежень".

### Значення, що повертаються

Функція не повертає значення після виконання.