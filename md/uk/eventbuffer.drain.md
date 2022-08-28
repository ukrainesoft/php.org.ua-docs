Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи

-   [« EventBuffer::copyout](eventbuffer.copyout.html)
    
-   [EventBuffer::enableLocking »](eventbuffer.enablelocking.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
    

# EventBuffer::drain

(PECL event >= 1.2.6-beta)

EventBuffer::drain — Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи

### Опис

```methodsynopsis
public
   EventBuffer::drain(
    int
     $len
   ): bool
```

Поводиться, як [EventBuffer::read()](eventbuffer.read.html), За винятком того, що він не копіює дані: просто видаляє їх з початку буфера.

### Список параметрів

`len`

Кількість байтів видалення з буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::read()](eventbuffer.read.html) - Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.html) - Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера