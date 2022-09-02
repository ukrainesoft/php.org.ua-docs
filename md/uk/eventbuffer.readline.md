---
navigation:
  - eventbuffer.readfrom.md: '« EventBuffer::readFrom'
  - eventbuffer.search.md: 'EventBuffer::search »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::readLine'
---
# EventBuffer::readLine

(PECL event >= 1.2.6-beta)

EventBuffer::readLine — Витягує рядок з початку буфера

### Опис

```methodsynopsis
public
   EventBuffer::readLine(
    int
     $eol_style
   ): string
```

Витягує рядок з початку буфера і повертає його в новому рядку. Якщо немає цілого рядка для читання, функція повертає **`null`**. Термінатор рядка не включається до скопійованого рядка.

### Список параметрів

`eol_style`

Одна з [EventBuffer:EOLконстант](class.eventbuffer.md#eventbuffer.constants)

### Значення, що повертаються

У разі успішного виконання повертає рядок, прочитаний з буфера, інакше повертає **`null`**

### Дивіться також

-   [EventBuffer::copyout()](eventbuffer.copyout.md) - Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.md) - Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::pullup()](eventbuffer.pullup.md) - Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
-   [EventBuffer::read()](eventbuffer.read.md) - Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.md) - Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера
