---
navigation:
  - eventbuffer.read.md: '« EventBuffer::read'
  - eventbuffer.readline.md: 'EventBuffer::readLine »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::readFrom'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Читає дані з файлу, указаного в `fd`в конец буфера.

### Список параметрів

`fd`

Ресурс сокету, потік чи числовий дескриптор файлу.

`howmuch`

Максимальна кількість байт для читання.

### Значення, що повертаються

Повертає кількість прочитаних байтів або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::copyout()](eventbuffer.copyout.md) \- Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.md) \- Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::pullup()](eventbuffer.pullup.md) \- Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
-   [EventBuffer::readLine()](eventbuffer.readline.md) \- Витягує рядок із початку буфера
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.md) \- Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера
