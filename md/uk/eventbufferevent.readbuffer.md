Зливає весь вміст буфера введення та поміщає його у буфер

-   [« EventBufferEvent::read](eventbufferevent.read.md)
    
-   [EventBufferEvent::setCallbacks »](eventbufferevent.setcallbacks.md)
    
-   [PHP Manual](index.md)
    
-   [EventBufferEvent](class.eventbufferevent.md)
    
-   Зливає весь вміст буфера введення та поміщає його у буфер
    

# EventBufferEvent::readBuffer

(PECL event >= 1.2.6-beta)

EventBufferEvent::readBuffer — Зливає весь вміст буфера введення та поміщає його в буфер

### Опис

```methodsynopsis
public
   EventBufferEvent::readBuffer(
    EventBuffer
     $buf
   ): bool
```

Зливає весь вміст буфера введення і поміщає його в `buf`

### Список параметрів

`buf`

Цільовий буфер

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBufferEvent::read()](eventbufferevent.read.md) - Читає дані буфера