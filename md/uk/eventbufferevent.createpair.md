---
navigation:
  - eventbufferevent.construct.md: '« EventBufferEvent::\_\_construct'
  - eventbufferevent.disable.md: 'EventBufferEvent::disable »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::createPair'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::createPair

(PECL event >= 1.2.6-beta)

EventBufferEvent::createPair — Створює дві буферні події, пов'язані один з одним

### Опис

```methodsynopsis
public
   static
   EventBufferEvent::createPair(
    EventBase
     $base
   , 
    int
     $options
     = 0
   ): array
```

Повертає масив із двох об'єктів [EventBufferEvent](class.eventbufferevent.md), пов'язані один з одним. Підтримуються всі звичайні параметри, крім **`EventBufferEvent::OPT_CLOSE_ON_FREE`**, який не діє, та **`EventBufferEvent::OPT_DEFER_CALLBACKS`**, який завжди включено.

### Список параметрів

`base`

Пов'язана основа подій.

`options`

Константи EventBufferEvent::OPT\_\* у поєднанні з побітовим АБО (`OR`

### Значення, що повертаються

Повертає масив із двох об'єктів [EventBufferEvent](class.eventbufferevent.md), пов'язані один з одним.

### список змін

| Версия | Опис |
| --- | --- |
| PECL event 1.9.0 | Метод став статичним. |
