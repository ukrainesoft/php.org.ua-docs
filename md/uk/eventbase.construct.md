---
navigation:
  - class.eventbase.md: « EventBase
  - eventbase.dispatch.md: 'EventBase::dispatch »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBase::\_\_construct

(PECL event >= 1.2.6-beta)

EventBase::\_\_construct — Конструктор об'єкту EventBase

### Опис

```methodsynopsis
public
   EventBase::__construct(
    EventConfig
     $cfg
    = ?)
```

Конструктор об'єкту EventBase.

### Список параметрів

`cfg`

Необов'язковий об'єкт [EventConfig](class.eventconfig.md)

### Помилки

Якщо об'єкт [EventBase](class.eventbase.md) не можна створити з наданою конфігурацією, буде викинуто виняток [EventException](class.eventexception.md)

### Дивіться також

-   [EventConfig](class.eventconfig.md)
