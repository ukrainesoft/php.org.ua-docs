---
navigation:
  - eventbuffer.construct.md: '« EventBuffer::\_\_construct'
  - eventbuffer.drain.md: 'EventBuffer::drain »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::copyout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Поводиться так само, як [EventBuffer::read()](eventbuffer.read.md)але не виводить дані з буфера. Тобто він копіює перші байти `max_bytes`с начала буфера в`data`. Якщо доступно менше `max_bytes`, функція копіює всі наявні байти.

### Список параметрів

`data`

Вихідний рядок.

`max_bytes`

Кількість байтів для копіювання.

### Значення, що повертаються

Повертає кількість скопійованих байтів або \*\*`-1`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::read()](eventbuffer.read.md) \- Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.md) \- Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера
