---
navigation:
  - eventbase.exit.md: '« EventBase::exit'
  - eventbase.getfeatures.md: 'EventBase::getFeatures »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::free'
---
# EventBase::free

(PECL event >= 1.10.0)

EventBase::free — Звільняє ресурси, виділені для цієї бази подій

### Опис

```methodsynopsis
public
   EventBase::free(): void
```

Визволяє ресурси, виділені якобов'язок для об'єкта [EventBase](class.eventbase.md)

**Увага**

Метод **EventBase::free()** не руйнує сам об'єкт. Щоб повністю знищити об'єкт, викличте [unset()](function.unset.md) або привласніть **`null`**

Цей метод не звільняє і не від'єднує будь-які події, які на даний момент пов'язані з об'єктом [EventBase](class.eventbase.md), і не закриває їх сокети - будьте обережні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventBase::construct()](eventbase.construct.md) - Конструктор об'єкту EventBase
