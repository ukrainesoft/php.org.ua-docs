Копіює вказану кількість байтів з початку буфера

-   [« EventBuffer::\_\_construct](eventbuffer.construct.html)
    
-   [EventBuffer::drain »](eventbuffer.drain.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Копіює вказану кількість байтів з початку буфера
    

# EventBuffer::copyout

(PECL event >= 1.2.6-beta)

EventBuffer::copyout — Копіює вказану кількість байтів з початку буфера

### Опис

```methodsynopsis
public
   EventBuffer::copyout(
    string
     &$data
   , 
    int
     $max_bytes
   ): int
```

Поводиться так само, як [EventBuffer::read()](eventbuffer.read.html)але не виводить дані з буфера. Тобто він копіює перші байти `max_bytes` з початку буфера в `data`. Якщо доступно менше `max_bytes`, функція копіює всі наявні байти.

### Список параметрів

`data`

Вихідний рядок.

`max_bytes`

Кількість байтів для копіювання.

### Значення, що повертаються

Повертає кількість скопійованих байтів або **`-1`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::read()](eventbuffer.read.html) - Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.html) - Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера