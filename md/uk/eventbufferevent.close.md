---
navigation:
  - class.eventbufferevent.md: « EventBufferEvent
  - eventbufferevent.connect.md: 'EventBufferEvent::connect »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::close

(PECL event >= 1.10.0)

EventBufferEvent::close — Закриває дескриптор файлу, пов'язаний із поточною подією буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::close(): void
```

Закриває дескриптор файлу, пов'язаний із поточною подією буфера.

Метод може використовуватись у тих випадках, коли опція \*\*`EventBufferEvent::OPT_CLOSE_ON_FREE`\*\*не подходит.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
