Додає вміст буфера в буфер виводу буферної події

-   [« EventBufferEvent::write](eventbufferevent.write.md)
    
-   [Про callback-функції подійного буфера](eventbufferevent.about.callbacks.md)
    
-   [PHP Manual](index.md)
    
-   [EventBufferEvent](class.eventbufferevent.md)
    
-   Додає вміст буфера в буфер виводу буферної події
    

# EventBufferEvent::writeBuffer

(PECL event >= 1.2.6-beta)

EventBufferEvent::writeBuffer — Додає вміст всього буфера в буфер виводу буферної події

### Опис

```methodsynopsis
public
   EventBufferEvent::writeBuffer(
    EventBuffer
     $buf
   ): bool
```

Додає вміст буфера в буфер виведення буферної події.

### Список параметрів

`buf`

Вихідний об'єкт [EventBuffer](class.eventbuffer.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBufferEvent::write()](eventbufferevent.write.md) - Додає дані до буфера виводу буферної події