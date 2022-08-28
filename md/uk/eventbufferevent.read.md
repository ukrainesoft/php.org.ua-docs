Читає дані буфера

-   [« EventBufferEvent::getOutput](eventbufferevent.getoutput.html)
    
-   [EventBufferEvent::readBuffer »](eventbufferevent.readbuffer.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Читає дані буфера
    

# EventBufferEvent::read

(PECL event >= 1.2.6-beta)

EventBufferEvent::read — Читає дані буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::read(
    int
     $size
   ): string
```

Видаляє до `size` байтів із вхідного буфера. Повертає рядок даних, прочитаний із вхідного буфера.

### Список параметрів

`size`

Максимальна кількість байтів для читання

### Значення, що повертаються

Повертає рядок даних, прочитаний із вхідного буфера.

### Дивіться також

-   [EventBufferEvent::readBuffer()](eventbufferevent.readbuffer.html) - Зливає весь вміст буфера введення та поміщає його у буфер