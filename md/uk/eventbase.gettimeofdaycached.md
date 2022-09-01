---
navigation:
  - eventbase.getmethod.md: '« EventBase::getMethod'
  - eventbase.gotexit.md: 'EventBase::gotExit »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::getTimeOfDayCached'
---
# EventBase::getTimeOfDayCached

(PECL event >= 1.2.6-beta)

EventBase::getTimeOfDayCached — Повертає поточний час базовий подій

### Опис

```methodsynopsis
public
   EventBase::getTimeOfDayCached(): float
```

При успішному завершенні повертає поточний час (як результат функції `gettimeofday()`), переглядаючи кешоване значення в *base*, якщо це можливо, і викликаючи `gettimeofday()` або `clock_gettime()`, Залежно від ситуації, якщо немає кешованого часу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний час *бази подій*. У разі виникнення помилки повертає **`null`**
