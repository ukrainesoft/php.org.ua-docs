Переміщає всі дані з буфера екземпляру EventBuffer

-   [« EventBuffer::add](eventbuffer.add.html)
    
-   [EventBuffer::appendFrom »](eventbuffer.appendfrom.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Переміщає всі дані з буфера екземпляру EventBuffer
    

# EventBuffer::addBuffer

(PECL event >= 1.2.6-beta)

EventBuffer::addBuffer — Переміщує всі дані з буфера екземпляру EventBuffer

### Опис

```methodsynopsis
public
   EventBuffer::addBuffer(
    EventBuffer
     $buf
   ): bool
```

Переміщує всі дані з буфера, вказаного у параметрі `buf`, в кінець поточного [EventBuffer](class.eventbuffer.html). Це руйнівний додаток. Дані з одного буфера переміщуються до іншого буфера. Однак, непотрібних копій пам'яті не відбувається.

### Список параметрів

`buf`

Вихідний об'єкт EventBuffer.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::add()](eventbuffer.add.html) - Додає дані до кінця буфера подій