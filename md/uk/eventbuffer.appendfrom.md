---
navigation:
  - eventbuffer.addbuffer.html: '« EventBuffer::addBuffer'
  - eventbuffer.construct.html: 'EventBuffer::construct »'
  - index.html: PHP Manual
  - class.eventbuffer.html: EventBuffer
title: 'EventBuffer::appendFrom'
---
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

| Версия | Описание |
| --- | --- |
| PECL event 1.6.0 | Перейменовано **EventBuffer::appendFrom()**(старе ім'я методу) **EventBuffer::appendFrom()** |

### Дивіться також

-   [EventBuffer::copyout()](eventbuffer.copyout.md) - Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.md) - Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::pullup()](eventbuffer.pullup.md) - Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
-   [EventBuffer::readLine()](eventbuffer.readline.md) - Витягує рядок із початку буфера
-   [EventBuffer::read()](eventbuffer.read.md) - Читає дані з evbuffer та виснажує прочитані байти
