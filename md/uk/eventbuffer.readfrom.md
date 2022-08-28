Читає дані з файлу до кінця буфера

-   [« EventBuffer::read](eventbuffer.read.html)
    
-   [EventBuffer::readLine »](eventbuffer.readline.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Читає дані з файлу до кінця буфера
    

# EventBuffer::readFrom

(PECL event >= 1.7.0)

EventBuffer::readFrom - Читає дані з файлу в кінець буфера

### Опис

```methodsynopsis
public
   EventBuffer::read(
    mixed
     $fd
   , 
    int
     $howmuch
   ): int
```

Читає дані з файлу, вказаного в `fd` в кінці буфера.

### Список параметрів

`fd`

Ресурс сокету, потік чи числовий дескриптор файлу.

`howmuch`

Максимальна кількість байт для читання.

### Значення, що повертаються

Повертає кількість прочитаних байтів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::copyout()](eventbuffer.copyout.html) - Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.html) - Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::pullup()](eventbuffer.pullup.html) - Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
-   [EventBuffer::readLine()](eventbuffer.readline.html) - Витягує рядок із початку буфера
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.html) - Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера