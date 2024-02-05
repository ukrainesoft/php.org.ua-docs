---
navigation:
  - eventbuffer.unlock.md: '« EventBuffer::unlock'
  - class.eventbufferevent.md: EventBufferEvent »
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::write'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::write

(PECL event >= 1.6.0)

EventBuffer::write — Записує вміст буфера у файл або сокет

### Опис

```methodsynopsis
public
   EventBuffer::write(
    mixed
     $fd
   , 
    int
     $howmuch
    = ?): int
```

Записує вміст буфера у дескриптор файлу. Буфер буде очищено після успішного запису байтів.

### Список параметрів

`fd`

Ресурс сокету, потоковий чи числовий дескриптор файлу, пов'язаний зазвичай із сокетом.

`howmuch`

Максимальна кількість байт для запису.

### Значення, що повертаються

Повертає кількість записаних байтів або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::read()](eventbuffer.read.md) \- Читає дані з evbuffer та виснажує прочитані байти
