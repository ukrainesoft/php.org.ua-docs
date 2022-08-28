Переміщує всі дані з вихідного буфера на початок поточного буфера

-   [« EventBuffer::prepend](eventbuffer.prepend.html)
    
-   [EventBuffer::pullup »](eventbuffer.pullup.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Переміщує всі дані з вихідного буфера на початок поточного буфера
    

# EventBuffer::prependBuffer

(PECL event >= 1.2.6-beta)

EventBuffer::prependBuffer — Переміщує всі дані з вихідного буфера на початок поточного буфера

### Опис

```methodsynopsis
public
   EventBuffer::prependBuffer(
    EventBuffer
     $buf
   ): bool
```

Поводиться як [EventBuffer::addBuffer()](eventbuffer.addbuffer.html) , За винятком того, що він переміщає дані на початок буфера.

### Список параметрів

`buf`

Початковий буфер.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::add()](eventbuffer.add.html) - Додає дані до кінця буфера подій
-   [EventBuffer::addBuffer()](eventbuffer.addbuffer.html) - Переміщує всі дані з буфера екземпляру EventBuffer
-   [EventBuffer::prepend()](eventbuffer.prepend.html) - Записує дані на початок буфера