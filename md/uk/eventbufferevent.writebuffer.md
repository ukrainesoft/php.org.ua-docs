Додає вміст буфера в буфер виводу буферної події

-   [« EventBufferEvent::write](eventbufferevent.write.html)
    
-   [О callback-функциях событийного буфера »](eventbufferevent.about.callbacks.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
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

Вихідний об'єкт [EventBuffer](class.eventbuffer.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBufferEvent::write()](eventbufferevent.write.html) - Додає дані до буфера виводу буферної події