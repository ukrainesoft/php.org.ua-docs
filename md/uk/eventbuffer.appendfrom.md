Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера

-   [« EventBuffer::addBuffer](eventbuffer.addbuffer.html)
    
-   [EventBuffer::\_\_construct »](eventbuffer.construct.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера
    

# EventBuffer::appendFrom

(PECL event >= 1.6.0)

EventBuffer::appendFrom — Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера

### Опис

```methodsynopsis
public
   EventBuffer::appendFrom(
    EventBuffer
     $buf
   , 
    int
     $len
   ): int
```

Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера. Якщо кількість байтів менша, переміщує всі байти, доступні з вихідного буфера.

### Список параметрів

`buf`

Початковий буфер.

`len`

### Значення, що повертаються

Повертає кількість прочитаних байтів.

### список змін

| Версия           | Описание                                                                                     |
|------------------|----------------------------------------------------------------------------------------------|
| PECL event 1.6.0 | Перейменовано **EventBuffer::appendFrom()**(старе ім'я методу) **EventBuffer::appendFrom()** |

### Дивіться також

-   [EventBuffer::copyout()](eventbuffer.copyout.html) - Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.html) - Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::pullup()](eventbuffer.pullup.html) - Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
-   [EventBuffer::readLine()](eventbuffer.readline.html) - Витягує рядок із початку буфера
-   [EventBuffer::read()](eventbuffer.read.html) - Читає дані з evbuffer та виснажує прочитані байти