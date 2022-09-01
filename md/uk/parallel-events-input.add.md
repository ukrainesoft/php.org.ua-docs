---
navigation:
  - class.parallel-events-input.html: « parallelEventsInput
  - parallel-events-input.clear.html: 'parallelEventsInput::clear »'
  - index.html: PHP Manual
  - class.parallel-events-input.html: parallelEventsInput
title: 'parallelEventsInput::add'
---
# parallelEventsInput::add

parallelEventsInput::add — Вхід

### Опис

```methodsynopsis
public parallel\Events\Input::add(string $target, mixed $value): void
```

Встановлює вхід для заданої мети

### Помилки

**Увага**

Викидає parallelEventsInputErrorExistence, якщо вхід до мети вже існує.

**Увага**

Викидає parallelEventsInputErrorIllegalValue, якщо значення неприпустимо (object, **`null`**
