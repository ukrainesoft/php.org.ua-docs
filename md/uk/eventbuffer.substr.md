---
navigation:
  - eventbuffer.searcheol.md: '« EventBuffer::searchEol'
  - eventbuffer.unfreeze.md: 'EventBuffer::unfreeze »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::substr'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::substr

(PECL event >= 1.6.0)

EventBuffer::substr — Обрізає частину даних буфера

### Опис

```methodsynopsis
public
   EventBuffer::substr(
    int
     $start
   , 
    int
     $length
    = ?): string
```

Обрізає до `length` байтів даних буфера, починаючи з позиції `start`

### Список параметрів

`start`

Початкова позиція даних, що підлягають обрізанню.

`length`

Максимальна кількість байт для обрізання.

### Значення, що повертаються

Повертає дані, вираховані у вигляді рядка (string) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::read()](eventbuffer.read.md) \- Читає дані з evbuffer та виснажує прочитані байти
