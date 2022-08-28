Надає пріоритет bufferevent

-   [« EventBufferEvent::setCallbacks](eventbufferevent.setcallbacks.html)
    
-   [EventBufferEvent::setTimeouts »](eventbufferevent.settimeouts.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Надає пріоритет bufferevent
    

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