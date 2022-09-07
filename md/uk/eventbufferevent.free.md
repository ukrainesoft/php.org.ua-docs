---
navigation:
  - eventbufferevent.enable.md: '« EventBufferEvent::enable'
  - eventbufferevent.getdnserrorstring.md: 'EventBufferEvent::getDnsErrorString »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::free'
---
# EventBufferEvent::free

(PECL event >= 1.2.6-beta)

EventBufferEvent::free — Звільняє подію буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::free(): void
```

Визволяє ресурси, виділені буферною подією.

Зазвичай немає необхідності викликати цей метод, оскільки це робиться у внутрішніх деструкторах об'єкта. Однак іноді скрипти виконуються довго і створюють безліч екземплярів, а іноді інтенсивно використовують пам'ять, тому необхідно якнайшвидше звільнити ресурси. У таких випадках **EventBufferEvent::free()** може використовуватися для захисту скрипту від досягнення `memory_limit`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
